<template>
  <div id="app">
    <navigation></navigation>
    <Main></Main>
  </div>
</template>

<script>
import Navigation from "./components/Navigation";
import Main from "./components/Main";

export default {
  name: "App",
  components: {
    Navigation,
    Main
  }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: purple;
}
</style>
