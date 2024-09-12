<template>
  <Navbar />
  <div class="test">
    <img alt="Vue logo" src="./assets/logo1.png" />
  </div>
  <ComingSoon />
  <!--  <BodyComponent /> -->
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
.test img {
  margin: 10px;
  height: 100px; /* Adjust the height as needed */
  width: auto;
}
</style>
