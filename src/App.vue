<template>
  <div id="app">
    <MyHeader />
    <MyMain />
  </div>
</template>

<script>
import MyHeader from "./components/MyHeader.vue";
import MyMain from "./components/MyMain.vue";
export default {
  name: "App",
  components: {
    MyHeader,
    MyMain,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
img {
  max-width: 100%;
}
#app {
  font-family: Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #1e2d3b;
  height: 100vh;
}
</style>
