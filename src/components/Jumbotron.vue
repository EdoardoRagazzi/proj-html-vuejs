<template>
  <div class="Jumbotron">
    <div class="wave">
      <img class="wave" src="..\assets\img\Wave-1.png" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Jumbotron",
};
</script>

<style scoped lang="scss">
@import "@/style/common.scss";
.wave {
  position: absolute;
  bottom: 0;

  img {
    color: white;
  }
}
</style>