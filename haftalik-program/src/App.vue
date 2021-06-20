<template>
  <div id="app">
    <days></days>
  </div>
</template>

<script>
import days from "./components/days";

export default {
  name: "App",
  components: {
    days
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 40px;
}
</style>
