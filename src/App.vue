<template>
  <div id="app">
    <Home></Home>
    <About></About>
    <services></services>
    <works></works>
    <Form></Form>
    <Footer></Footer>
  </div>
</template>

<script>
import Home from "./components/Home.vue";
import About from "./components/About.vue";
import Services from "./components/Services.vue";
import Works from "./components/Works.vue";
import Form from "./components/Form.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Home,
    About,
    Services,
    Works,
    Form,
    Footer,
  },
};
</script>

<style>
@import "./assets/styles/style.css";
</style>
