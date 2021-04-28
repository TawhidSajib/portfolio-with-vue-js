<template>
  <div id="app">
    <portfolio></portfolio>
  </div>
</template>

<script>
import portfolio from "./components/portfolio.vue";

export default {
  name: "App",
  components: {
    portfolio,
  },
};
</script>

<style>
@import "./assets/styles/style.css";
</style>
