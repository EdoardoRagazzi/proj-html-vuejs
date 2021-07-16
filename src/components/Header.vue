<template>
  <div class="header">
    <Nav />
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
};
</script>

<style scoped lang="scss">
@import "@/style/common.scss";
.header {
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
    /* bottom, image */ url("../assets/img/theme_slider1_bg-1.jpg");
}
</style>