<template>
  <div class="thirdslide">
    <div class="slide">
      <div class="card">
        <img src="..\assets\img\Exam-icon.png" alt="" />
        <h5 class="card-title text-uppercase">
          Thousands of courses for any type of student
        </h5>
        <p class="card-text">
          At EduPrime, it doesn’t matter what domain you wish to pursue a career
          in. Here you can find a course that satisfies your needs within a
          click away and applies for a course in a matter of minutes. EduPrime
          is ranked as the most versatile university in the world, thanks to the
          number of courses it provides.
        </p>
        <a href="#" class="btn btn-primary">Browse through courses</a>
      </div>
      <div class="image">
        <img src="..\assets\img\Exam-Illustration.png" alt="" />
      </div>
    </div>
    <div class="slide">
      <div class="image">
        <img src="..\assets\img\Girl-Illustration.png" alt="" />
      </div>
      <div class="card">
        <img src="..\assets\img\Exam-icon-1.png" alt="" />
        <h5 class="card-title text-uppercase">
          Thousands of courses for any type of student
        </h5>
        <p class="card-text">
          At EduPrime, it doesn’t matter what domain you wish to pursue a career
          in. Here you can find a course that satisfies your needs within a
          click away and applies for a course in a matter of minutes. EduPrime
          is ranked as the most versatile university in the world, thanks to the
          number of courses it provides.
        </p>
        <a href="#" class="btn btn-primary">Browse through courses</a>
      </div>
    </div>
    <div class="picturecard">
      <h1>Latest Blog Posts</h1>
      <div class="cards d-flex justify-content-center">
        <div class="card" style="width: 30rem">
          <img src="..\assets\img\SmartOWL.jpg" class="card-img-top" alt="" />
          <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
            <a href="#" class="btn btn-primary"
              ><i class="bi bi-chevron-right"></i
            ></a>
          </div>
        </div>
        <div class="card" style="width: 30rem">
          <img src="..\assets\img\SmartOWL.jpg" class="card-img-top" alt="" />
          <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
            <a href="#" class="btn btn-primary"
              ><i class="bi bi-chevron-right"></i
            ></a>
          </div>
        </div>
        <div class="card" style="width: 30rem">
          <img src="..\assets\img\SmartOWL.jpg" class="card-img-top" alt="" />
          <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
            <a href="#" class="btn btn-primary"
              ><i class="bi bi-chevron-right"></i
            ></a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Thirdslide",
};
</script>


<style scoped lang="scss">
@import "@/style/common.scss";

.picturecard {
  width: 100%;
  float: left;
  padding-top: 100px;
  text-align: left;
  .card {
    margin: 30px;
    box-shadow: 0 4px 8px 0 #8d898933, 0 6px 20px 0 #8d898933;
    img {
      transition: transform 0.8s;
      &:hover {
        transform: scale(1.1);
        cursor: pointer;
      }
    }
    .btn {
      max-width: 100px;
      float: right;
      /* margin-top: 20px; */
      max-width: 300px;
      /* height: 60px; */
      text-align: center;
      vertical-align: middle;
      border: 0px;
      background: #e9d758;
      /* padding: 16px 43px !important; */
      border-radius: 50px;
      margin-left: 20px;
      letter-spacing: 0.5px;
      color: #fff;
      transition: all 300ms ease;
      -webkit-transition: all 300ms ease;
      &:hover {
        background-color: #e56768;
        margin-top: -10px;
      }
    }
  }
}

.thirdslide {
  margin-left: 100px;
  margin-right: 100px;
  margin-top: 100px;
  height: 1500px;
  width: 1350px;
}
.slide {
  width: 100%;
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
.slide {
  .card {
    float: left;
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
}
</style>