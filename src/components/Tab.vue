<template>
  <div class="tab">
    <div class="card">
      <h5 class="card-title text-uppercase">Thousands of courses</h5>
      <p class="card-text">
        At EduPrime, it doesn’t matter what domain you wish to pursue a career
        in. Here you can find!!!
      </p>
    </div>
    <div class="tabs d-flex justify-content-center">
      <div
        class="nav d-flex justify-content-center"
        v-for="(item, index) in navs"
        :key="index"
        @click="changeUtente(index)"
      >
        <img :src="iconSrc(item.image)" alt="" />
        <span>{{ item.text }}</span>
      </div>
    </div>
    <div class="showtab d-flex justify-content-center">
      <div class="image">
        <img :src="iconSrc(navs[this.counter].postimage)" alt="" />
      </div>
      <div class="text">
        <h3>{{ navs[this.counter].text }}</h3>
        <br />
        <p>{{ navs[this.counter].context }}</p>
        <button>Read More</button>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "../data/Card.js";
export default {
  name: "Tab",
  data() {
    return {
      navs: Card,
      counter: 0,
    };
  },
  methods: {
    iconSrc(icon) {
      return require("../assets/" + icon);
    },

    changeUtente(index) {
      this.counter = index;
    },
  },
};
</script>


<style scoped lang="scss">
@import "@/style/common.scss";
.tabs {
  border-bottom: 1px solid grey;
  border-top: 1px solid grey;

  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
.tab {
  width: 100%;
  height: 100%;

  .nav {
    width: 200px;
    text-align: center;
    border: 1px solid grey;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    span {
      font-family: "Fredoka One";
      color: #e56768;
    }
    &:hover {
      cursor: pointer;
      background-color: #e56768;

      img,
      span {
        -webkit-filter: brightness(0) invert(1);
        filter: brightness(0) invert(1);
      }
    }
  }
}

img {
  padding-top: 20px;
  height: 100px;
  width: 150px;
  margin-bottom: 20px;
  display: block;
}
span {
  padding-top: 10px;
  text-align: center;
}

.card {
  float: center;
  text-align: center;
  border: 1px solid white;
  margin-bottom: 20px;

  .card-title {
    font-family: "Fredoka One";
    font-weight: 600;
    font-size: 30px;
    color: #3d404f;
  }
}
.showtab {
  padding-top: 100px;
  height: 400px;
  width: 100%;
  font-family: "Fredoka One";
  button {
    background-color: #e56768;
    border: 0px;
    color: white;
    border-radius: 50px;
    height: 70px;
    width: 150px;
    &:hover {
      background-color: #e9d758;
    }
  }
  .image {
    margin-right: 50px;
    height: 250px;
    width: 300px;
    img {
      height: 100%;
      width: 100%;
    }
  }
  .text {
    max-width: 400px;
    padding-left: 20px;

    h3 {
      font-weight: 600;
      font-size: 50px;
    }
    p {
      color: lightgrey;
      font-weight: 200;
    }
  }
}
</style>

