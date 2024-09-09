<template>
  <Navbar />
  <BodyComponent />
  <img alt="Vue logo" src="./assets/logo.png" />
</template>

<script>
import HelloWorldVue from "./components/HelloWorld.vue";
import Navbar from "./components/Navbar.vue";
import BodyComponent from "./components/Center.vue";
export default {
  name: "App",
  components: {
    HelloWorld: HelloWorldVue,
    Navbar,
    BodyComponent,
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
