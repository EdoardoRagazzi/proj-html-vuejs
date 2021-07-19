<template>
  <div class="Nav d-flex justify-content-around">
    <img src="..\assets\img\theme_eduprime_logo.png" alt="" />
    <b-navbar type="dark">
      <b-navbar-nav
        v-for="(item, index) in navs"
        :key="index"
        :class="{ activeitem: item.current }"
      >
        <b-nav-item-dropdown
          type="dark"
          class="drop"
          :text="item.text"
          right
          v-if="item.arrow == true"
          :href="item.url"
          :class="{ activelink: item.current }"
        >
          <b-dropdown-item href="#">EN</b-dropdown-item>
          <b-dropdown-item href="#">ES</b-dropdown-item>
          <b-dropdown-item href="#">RU</b-dropdown-item>
          <b-dropdown-item href="#">FA</b-dropdown-item>
        </b-nav-item-dropdown>

        <b-nav-item
          class="drop"
          v-else-if="item.arrow == false && item.button == false"
          :href="item.url"
          :class="{ activelink: item.current }"
          >{{ item.text }}</b-nav-item
        >
        <b-nav-item
          class="drop button"
          v-else
          :href="item.url"
          :class="{ activelink: item.current }"
          >{{ item.text }}</b-nav-item
        >
      </b-navbar-nav>
    </b-navbar>
  </div>
</template>

<script>
import NavsItems from "../data/Navs.js";
export default {
  name: "Nav",
  data() {
    return {
      navs: NavsItems,
    };
  },
};
</script>

<style scoped lang="scss">
@import "@/style/common.scss";
.Nav {
  padding-top: 40px;
  position: absolute;
  top: 3%;
  width: 100%;
  z-index: 999;
}
img {
  height: 60px;
  max-width: 270px;
}
b-navbar {
  height: 115px;
  color: white;

  img {
    padding: 10px;
  }

  a {
    text-decoration: none;
    color: white;
  }
}
.drop {
  font-weight: 900;
  #__BVID__7__BV_toggle_ {
    color: white;
    span {
      color: white;
    }
  }
}
.button {
  line-height: 20px;
  height: 70px;
  max-width: 250px;
  text-align: center;
  vertical-align: middle;
  border: 0px;
  background: #e9d758;
  padding: 16px 43px !important;
  border-radius: 50px;
  text-transform: uppercase !important;
  margin-left: 20px;
  letter-spacing: 0.5px;
  color: #fff;
  cursor: pointer;
  transition: all 300ms ease;
  -webkit-transition: all 300ms ease;
  &:hover {
    background-color: white;
    cursor: pointer;

    a.nav-link {
      color: red;
    }
  }
}

// NAVBAR COLORs TRIED BUT WITHOUT RESULTS
// .navbar-dark .navbar-nav .nav-link {
//   color: white;
// }
// nav .navbar-nav li a {
//   color: white !important;
// }
// .navbar-light .navbar-nav .nav-link {
//   color: white !important;
// }
// .navbar-dark .navbar-nav .nav-link {
//   color: white;
// }
// .navbar.navbar-dark.bg-dark {
//   background-color: white !important;
// }
</style>
   