<template>
  <div class="menagement">
    <div class="newsletter">
      <div class="tab d-flex justify-content-around">
        <div class="text">
          <h1>Subscribe Now to Our Newsletter!</h1>
        </div>
        <div class="input">
          <input type="text" placeholder="Email Address..." />
          <button type="submit">
            <i class="bi bi-layer-forward"></i>
          </button>
        </div>
      </div>
    </div>
    <div class="menage">
      <div class="text">
        <h1>Menagement</h1>
        <p>
          A team of expert teachers that are leading our university! Meet our
          staff and become a student at EduPrime this year!
        </p>
      </div>
      <div class="avatarslide d-flex justify-content-center align-items-center">
        <div class="slide">
          <button class="btn"><i class="bi bi-caret-left"></i></button>
        </div>
        <div class="slide">
          <img src="../assets/img/avatar.png" alt="" />
        </div>
        <div class="slide">
          <img src="../assets/img/avatar.png" alt="" />
        </div>
        <div class="slide">
          <img src="../assets/img/avatar.png" alt="" />
        </div>
        <div class="slide">
          <img src="../assets/img/avatar.png" alt="" />
        </div>
        <div class="slide">
          <button class="btn"><i class="bi bi-caret-right"></i></button>
        </div>
      </div>
      <div class="teambutton"><button class="btn">View All team</button></div>
    </div>
    <div class="partners">
      <div class="text">
        <h1>Partners</h1>
        <p>
          Leverage agile frameworks to provide a robust synopsis for high level
          overviews. Iterative approaches to corporate strategy.
        </p>
      </div>
      <div class="icons d-flex justify-content-center">
        <div class="icon">
          <img src="..\assets\img\partner-1.png" alt="" />
        </div>
        <div class="icon">
          <img src="..\assets\img\partner-2.png" alt="" />
        </div>
        <div class="icon">
          <img src="..\assets\img\partner-3.png" alt="" />
        </div>
        <div class="icon">
          <img src="..\assets\img\partner-4.png" alt="" />
        </div>
        <div class="icon">
          <img src="..\assets\img\partner-5.png" alt="" />
        </div>
        <div class="icon">
          <img src="..\assets\img\partner-6.png" alt="" />
        </div>
        <div class="icon">
          <img src="..\assets\img\partner-7.png" alt="" />
        </div>
        <div class="icon">
          <img src="..\assets\img\partner-8.png" alt="" />
        </div>
      </div>
    </div>
    <div class="carousel">
      <h1>Thoughts from our students</h1>
      <div class="carouselslide">
        <hooper :itemsToShow="2" style="height: 400px">
          <slide v-for="(item, index) in navs" :key="index">
            <div class="card m-3" style="max-width: 30rem">
              <div
                class="card-header bg-transparent border-success text-danger"
              >
                <img :src="iconSrc(item.postimage)" alt="" /> {{ item.text }}
              </div>
              <div class="card-body">
                <h5 class="card-title"></h5>
                <p class="card-text">
                  {{ item.context }}
                </p>
              </div>
              <div class="card-footer bg-transparent border-success">
                <img :src="iconSrc(item.image)" alt="" />
                {{ item.text }}
              </div>
            </div>
          </slide>
        </hooper>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "../data/Card.js";
import { Hooper, Slide } from "hooper";
import "hooper/dist/hooper.css";
export default {
  name: "Subscribe",
  components: {
    Hooper,
    Slide,
  },
  data() {
    return {
      navs: Card,
    };
  },
  methods: {
    iconSrc(icon) {
      return require("../assets/" + icon);
    },
  },
};
</script>


<style scoped lang="scss">
@import "@/style/common.scss";
.newsletter {
  height: 200px;
  background-color: #e56768;

  .tab {
    padding-top: 70px;
    font-family: "Fredoka One";
    color: white;
  }
  .input {
    position: relative;
  }
  input {
    border-radius: 35px;
    height: 70px;
    font-size: 15px;
    border: 0 none;
    float: left;
    padding: 25px;
    width: 700px;
    font-weight: 400;
    outline: 0;
  }
  button {
    position: absolute;
    top: 0;
    height: 70px;
    padding: 21px 28px;
    background: #e9d758;
    border-radius: 50%;
    right: -1px;
    color: #fff;
    font-size: 20px;
    box-shadow: none;
    border: 0;
    outline: 0;
    box-shadow: 0px 0px 20px rgb(0 0 0 / 7%);
    transition: all 300ms ease;
    -webkit-transition: all 300ms ease;
    &:hover {
      background-color: #e56768;
    }
  }
}
.avatarslide {
  margin: auto;
  width: 70%;
}
.menage {
  margin-top: 50px;
  .img {
    border-radius: 50%;
    height: 150px;
    width: 150px;
    vertical-align: middle;
  }
  .btn {
    max-width: 100px;
    /* margin-top: 20px; */
    /* height: 60px; */
    text-align: center;
    vertical-align: middle;
    border: 0px;
    background-color: #e56768;
    /* padding: 16px 43px !important; */
    border-radius: 50px;

    letter-spacing: 0.5px;
    color: #fff;
    transition: all 300ms ease;
    -webkit-transition: all 300ms ease;
    &:hover {
      background: #e9d758;
      margin-top: -10px;
    }
  }
  .teambutton {
    margin-top: 150px;
    .btn {
      height: 80px;
      background: #e9d758;
      min-width: 300px;
      border-radius: 50px;
      letter-spacing: 0.5px;

      vertical-align: middle;
      text-align: center;
      &:hover {
        background-color: #e56768;
        margin-top: 0px;
      }
    }
  }
}
.partners {
  width: 80%;
  margin: 40px auto;
  img {
    height: 80px;
    width: 160px;
    padding: 10px;
    opacity: 0.3;
    &:hover {
      cursor: pointer;
      opacity: 1;
    }
  }
}
.carousel {
  height: 100%;
  width: 100%;
  background-image: url("../assets/img/background-wave3.png");
  background-size: 100% 100%;
  background-color: #f7f8fa;
  margin-top: 100px;
  font-family: "Fredoka One";
  font-weight: 600;
  font-size: 30px;
  color: #3d404f;
  .carouselslide {
    padding: 20px;
    height: 80%;
    width: 60%;
    margin: auto;
    img {
      height: 100px;
      width: 100px;
      float: left;
    }
    .card-text {
      font-size: 10px;
    }
  }
}
</style>