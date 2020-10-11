<template>
  <div id="app">
    <HelloWorld />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld
  }
};
</script>

<style>
#app {
  font-family: "Roboto", sans-serif;
  text-align: center;
  margin: 1rem;
}
body {
  background-color: #1a202c;
  color: #2c3e50;
}
</style>
