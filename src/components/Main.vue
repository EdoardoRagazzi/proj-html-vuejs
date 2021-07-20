<template>
  <div class="main">
    <div class="firstslide">
      <Firstslide class="slide" />
    </div>
    <div>
      <Tab />
    </div>
  </div>
</template>

<script>
import Firstslide from "@/components/Firstslide.vue";
import Tab from "@/components/Tab.vue";
export default {
  name: "Main",
  components: {
    Firstslide,
    Tab,
  },
};
</script>


<style scoped lang="scss">
@import "@/style/common.scss";
.main {
  height: 100%;
}
.firstslide {
  height: 500px;
  margin-top: 50px;

  width: 100%;
  background-image: url(../assets/img/home-background.png);
  background-size: 100% 100%;
  background-repeat: no-repeat;
  opacity: 2;
  z-index: 1;
}
</style>