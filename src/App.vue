<template>
  <div id="app">
    <div class="btn-sticky-left">
      <i class="bi bi-archive"></i>
      <i class="bi bi-bag"></i>
      <i class="bi bi-cart"></i>
    </div>
    <div class="mt_trigger-overlay first">
      <a href="#"><i class="bi bi-cloud-fill"></i>Edoardo Ragazzi</a>
    </div>
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
};
</script>

<style lang="scss">
@import "@/style/common.scss";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.btn-sticky-left {
  background: #e9d758 none repeat scroll 0 0;
  border-radius: 0 5px 5px 0;
  box-shadow: 0 0 25px rgb(37 37 37 / 40%);
  left: 0;
  z-index: 1000;
  position: fixed;
  top: 35%;
  i {
    margin: 30px;
    display: block;
    color: white;
    cursor: pointer;
    transition: transform 0.8s;
    &:hover {
      transform: scale(2);
    }
  }
  &:hover {
    padding-left: 20px;
  }
}
.mt_trigger-overlay {
  width: 200px;
  z-index: 222222;
  transition: all 250ms ease-in-out;
  -webkit-transition: all 250ms ease-in-out;
  position: fixed;
  left: 40px;
  font-weight: 300;
  bottom: 40px;
  background: #454545;
  color: #fff;
  padding: 10px 25px;
  letter-spacing: 0.5px;
  cursor: pointer;
  box-shadow: 0 17px 10px -12px rgba(0, 0, 0, 0.4) !important;
  -webkit-box-shadow: 0 17px 10px -12px rgba(0, 0, 0, 0.4) !important;
  border-radius: 5px;
  font-size: 1em;
  a {
    text-decoration: none;
    color: rgb(127, 163, 127);
  }
  &:hover {
    bottom: 50px;
  }
}
</style>
