<template>
  <div>
    <section class="services">
      <article class="container">
        <header>
          <h2 class="service-header">Amazing Services</h2>
          <p class="service-para">We provide quality services</p>
        </header>
        <div class="row justify-center wrap">
          <div class="col-33" v-for="(user, index) in myJson.data" :key="index">
            <div class="serviceColumn">
              <h1 class="service-header">{{ user.header }}</h1>
              <p class="service-para">{{ user.paragraph }}</p>
            </div>
          </div>
        </div>
      </article>
    </section>
  </div>
</template>
 <script>
import user from "@/assets/json/user.json";
export default {
  data() {
    return {
      myJson: user,
      display: true,
    };
  },
};
</script>