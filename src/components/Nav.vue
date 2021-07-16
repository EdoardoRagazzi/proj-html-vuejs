<template>
  <div class="Nav d-flex justify-content-around">
    <img src="..\assets\img\theme_eduprime_logo.png" alt="" />
    <nav>
      <ul>
        <li
          v-for="(item, index) in navs"
          :key="index"
          :class="{ activeitem: item.current }"
        >
          <a :href="item.url" :class="{ activelink: item.current }">{{
            item.text
          }}</a>
        </li>
      </ul>
    </nav>
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
img {
  height: 100px;
  width: 300px;
}
.Nav {
  height: 115px;
  line-height: 100px;

  img {
    padding: 5px;
  }
  ul {
    padding-left: 50px;
    list-style: none;
    li {
      display: inline-block;
      padding: 5px;
      list-style: none;

      &:hover {
        color: blue;
        border-bottom: 5px solid blue;
        transition: 0.5s ease;
      }
      a {
        text-decoration: none;

        color: white;
        font-size: 20px;
        font-weight: 600;
      }
    }
  }
}
</style>