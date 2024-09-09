<template>
  <Navbar />
  <ComingSoon />
  <!--  <BodyComponent /> -->
  <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
</template>

<script>
import Navbar from "./components/Navbar.vue";
import ComingSoon from "./components/Comingsoon.vue";
export default {
  name: "App",
  components: {
    Navbar,
    ComingSoon,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
