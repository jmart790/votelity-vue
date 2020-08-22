<template>
  <div id="app">
    <Home />
  </div>
</template>

<script>
import Home from "./views/Home";
export default {
  components: { Home }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Montserrat:400,500,600&display=swap");
#app {
  font-family: "Montserrat", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
* {
  padding: 0;
  margin: 0;
}
</style>
