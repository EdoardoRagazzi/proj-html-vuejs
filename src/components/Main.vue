<template>
  <div class="main">
    <div class="firstslide">
      <Firstslide class="slide" />
    </div>
  </div>
</template>

<script>
import Firstslide from "@/components/Firstslide.vue";
export default {
  name: "Main",
  components: {
    Firstslide,
  },
};
</script>


<style scoped lang="scss">
@import "@/style/common.scss";
.firstslide {
  margin-top: 50px;
  height: 500px;
  width: 100%;
  background-image: url(../assets/img/home-background.png);
  background-size: 100% 100%;
  opacity: 2;
  z-index: 2000;
}
.slide {
}
</style>