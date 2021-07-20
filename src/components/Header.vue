<template>
  <div class="header">
    <b-carousel
      id="carousel-1"
      :interval="10000"
      controls
      indicators
      img-height="100%"
      img-width="1024"
      style="text-shadow: 1px 1px 2px #333"
    >
      <!-- v-model="slide" -->
      <Nav />
      <!-- Text slides with image -->

      <!-- Slides with img slot -->
      <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="..\assets\img\theme_slider1_bg-1.jpg"
            alt="image slot"
            blank-color="#777"
            text="Nulla vitae elit libero, a pharetra augue mollis interdum."
          />
        </template>
        <h1>
          Show case your course
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste, quas?
            <br />
            Lorem ipsum dolor sit amet.
          </p>
          <b-button class="btn btn-left" pill>
            <i class="bi bi-search"></i> Search courses
          </b-button>
          <b-button class="btn btn-right" pill>
            <i class="bi bi-person-plus"></i>Apply for university</b-button
          >
        </h1>
      </b-carousel-slide>
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="..\assets\img\theme_slider2_bg-1.jpg"
            alt="image slot"
            text="Nulla vitae elit libero, a pharetra augue mollis interdum."
          />
        </template>
        <h1>
          Key to your success!
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste, quas?
            <br />
            Lorem ipsum dolor sit amet.
          </p>
          <b-button class="btn btn-left" pill>
            <i class="bi bi-search"></i> Search courses
          </b-button>
          <b-button class="btn btn-right" pill>
            <i class="bi bi-person-plus"></i>Apply for university</b-button
          >
        </h1>
      </b-carousel-slide>
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="..\assets\img\theme_slider3_bg-1.jpg"
            alt="image slot"
            text="Nulla vitae elit libero, a pharetra augue mollis interdum."
          />
        </template>
        <h1>
          Lead.Inspire.Win!
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste, quas?
            <br />
            Lorem ipsum dolor sit amet.
          </p>
          <b-button class="btn btn-left" pill>
            <i class="bi bi-search"></i> Search courses
          </b-button>
          <b-button class="btn btn-right" pill>
            <i class="bi bi-person-plus"></i>Apply for university</b-button
          >
        </h1>
      </b-carousel-slide>
      <Jumbotron />
      <!-- Slide with blank fluid image to maintain slide aspect ratio -->
    </b-carousel>
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";
import Jumbotron from "@/components/Jumbotron.vue";
export default {
  name: "Header",
  components: {
    Nav,
    Jumbotron,
  },
  // data() {
  //   return {
  //     slide: 0,
  //     sliding: null,
  //   };
  // },
  // methods: {
  //   onSlideStart(slide) {
  //     this.sliding = true;
  //   },
  //   onSlideEnd(slide) {
  //     this.sliding = false;
  //   },
  // },
};
</script>

<style scoped lang="scss">
@import "@/style/common.scss";

.sr-only {
  font-size: 0.2px;
  display: none;
}
.header {
  position: relative;
  top: 0;
  background-repeat: no-repeat;
  background-size: 100% 100%;
  height: 100%;
  width: 100%;
  background: 
    /* top, transparent red, faked with gradient */ linear-gradient(
    #dc6d6d,
    #dc6d6d
  );

  img {
    opacity: 0.1;
  }
}

h1 {
  padding-bottom: 80px;
  z-index: 6;
  font-family: "Fredoka One";
  text-align: center;
  height: auto;
  width: auto;
  color: rgb(255, 255, 255);
  text-decoration: none;
  white-space: nowrap;
  min-height: 0px;
  min-width: 0px;
  max-height: none;
  max-width: none;
  text-align: inherit;
  line-height: 60px;
  letter-spacing: 0px;
  font-weight: 900;
  text-align: center;
  font-size: 80px;
}
p {
  text-align: center;
  padding-top: 30px;
  font-size: 30px;
  font-weight: 300;
  color: white;
  font-family: "Fredoka One";
}
.btn {
  height: 70px;
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
.btn-right {
  color: rgb(145, 59, 59);
  background-color: white;
  &:hover {
    background-color: #e9d758;
    color: white;
  }
}
</style>