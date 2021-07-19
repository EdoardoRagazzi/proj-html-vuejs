<template>
  <div class="firstslide">
    <div class="card">
      <img src="../assets/img/Books-icon.png" alt="" />
      <h5 class="card-title text-uppercase">
        Thousands of courses for any type of student
      </h5>
      <p class="card-text">
        At EduPrime, it doesn’t matter what domain you wish to pursue a career
        in. Here you can find a course that satisfies your needs within a click
        away and applies for a course in a matter of minutes. EduPrime is ranked
        as the most versatile university in the world, thanks to the number of
        courses it provides.
      </p>
      <a href="#" class="btn btn-primary">Browse through courses</a>
    </div>
    <div class="image">
      <img src="..\assets\img\Graduation-Illustration.png" alt="" />
    </div>
  </div>
</template>

<script>
import Card from "../data/Card.js";
export default {
  name: "Firstslide",
  data() {
    return {
      navs: Card,
    };
  },
};
</script>


<style scoped lang="scss">
@import "@/style/common.scss";
.btn {
  margin-top: 20px;
  max-width: 300px;
  height: 60px;
  text-align: center;
  vertical-align: middle;
  border: 0px;
  background: #e9d758;
  padding: 16px 43px !important;
  border-radius: 50px;
  margin-left: 20px;
  letter-spacing: 0.5px;
  color: #fff;
  transition: all 300ms ease;
  -webkit-transition: all 300ms ease;
  &:hover {
    background-color: white;
    color: rgb(15, 13, 13);
    a.nav-link {
      color: red;
    }
  }
}
.btn-left {
  color: white;
  background-color: #e9d758;
  &:hover {
    background-color: white;
    color: rgb(145, 59, 59);
  }
}
.image {
  float: left;
  img {
    height: 400px;
    width: 600px;
  }
}
.card {
  float: left;
  padding-left: 100px;
  width: 700px;
  border: 1px solid white;
  text-align: justify;
  img {
    height: 50px;
    width: 50px;
    margin-bottom: 20px;
  }
  .card-title {
    font-family: "Fredoka One";
    font-weight: 600;
    font-size: 30px;
    color: #3d404f;
  }
}
</style>