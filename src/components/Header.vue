<template>
  <div class="header">
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="100%"
      style="text-shadow: 1px 1px 2px #333"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <Nav />
      <!-- Text slides with image -->
      <b-carousel-slide
        caption="First slide"
        text="Nulla vitae elit libero, a pharetra augue mollis interdum."
        img-src="https://github.com/EdoardoRagazzi/proj-html-vuejs/blob/0a9d92d39f50d45f1baa9f52af80515f8e81bc2c/src/assets/img/theme_slider1_bg-1.jpg"
      ></b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide
        img-src="https://github.com/EdoardoRagazzi/proj-html-vuejs/blob/0a9d92d39f50d45f1baa9f52af80515f8e81bc2c/src/assets/img/theme_slider1_bg-1.jpg"
      >
        <h1>Hello world!</h1>
      </b-carousel-slide>

      <!-- Slides with image only -->
      <b-carousel-slide
        img-src="https://github.com/EdoardoRagazzi/proj-html-vuejs/blob/0a9d92d39f50d45f1baa9f52af80515f8e81bc2c/src/assets/img/theme_slider1_bg-1.jpg"
      ></b-carousel-slide>

      <!-- Slides with img slot -->
      <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="https://picsum.photos/1024/480/?image=55"
            alt="image slot"
          />
        </template>
      </b-carousel-slide>

      <!-- Slide with blank fluid image to maintain slide aspect ratio -->
      <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse
          eros felis, tincidunt a tincidunt eget, convallis vel est. Ut
          pellentesque ut lacus vel interdum.
        </p>
      </b-carousel-slide>
    </b-carousel>

    <p class="mt-4">
      Slide #: {{ slide }}<br />
      Sliding: {{ sliding }}
    </p>

    <Jumbotron />
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
  data() {
    return {
      slide: 0,
      sliding: null,
    };
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true;
    },
    onSlideEnd(slide) {
      this.sliding = false;
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/style/common.scss";
.header {
  position: absolute;
  top: 0;
  // background-image: url("../assets/img/theme_slider1_bg-1.jpg");
  background-repeat: no-repeat;
  background-size: 100% 100%;
  height: 100vh;
  width: 100%;
  background: 
    /* top, transparent red, faked with gradient */ linear-gradient(
      rgba(255, 0, 0, 0.45),
      rgba(255, 0, 0, 0.45)
    ),
    /* bottom, image */ url("");
}
</style>