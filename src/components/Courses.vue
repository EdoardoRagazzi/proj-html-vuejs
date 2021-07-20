<template>
  <div class="courses">
    <h1>Latest Courses</h1>
    <div class="typecourses">
      <div class="card" v-for="(item, index) in courses" :key="index">
        <div class="card-body">
          <img :src="iconSrc(item.image)" alt="" />
          <div class="card-date">
            <i class="bi bi-calendar3"></i>24 Mar 18:00 PM
          </div>
          <p class="card-text">
            {{ item.text }}
          </p>
          <div><i class="bi bi-person"></i>Teacher: {{ item.teacher }}</div>
          <br />
          <div><i class="bi bi-cash"></i>Price: {{ item.price }}</div>
          <a href="#" class="btn btn-primary"
            ><i class="bi bi-plus-lg"></i>Find More</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Courseitems from "../data/Courses.js";
export default {
  name: "Courses",
  data() {
    return {
      courses: Courseitems,
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
span {
  padding-bottom: 10px;
}
.typecourses {
  display: flex;
  justify-content: center;
  .card {
    margin: 20px;
    border-radius: 25px;
    min-width: 270px;
    max-height: 300px;
    box-shadow: 0 3px 10px rgb(0 0 0 / 0.2);
    .card-date {
      margin-top: 20px;
    }
    p {
      color: $gray-600;
    }
    .btn {
      margin-top: 20px;
      height: 50px;
      border-radius: 25px;
      vertical-align: middle;
      padding: 16px 43px !important;
      background-color: #e56768;
      box-shadow: 0 3px 10px rgb(0 0 0 / 0.2);
      border: 0px;
      &:hover {
        background-color: #e9d758;
      }
    }
    img {
      height: 80px;
      width: 100px;
      transition: transform 0.8s;
      &:hover {
        transform: scale(1.1);
      }
    }
  }
}
</style>