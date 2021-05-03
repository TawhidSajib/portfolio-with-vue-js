<template>
  <div>
    <header>
      <nav class="container row space-between">
        <h2 class="logoName">Tawhid</h2>
        <ul
          class="nav-list"
          :class="[display ? 'displayNone' : 'displayBlock']"
        >
          <li class="nav-item">
            <a class="nav-link" href="#">HOME</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">FEATURES</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">CONTACT US</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">BLOG</a>
          </li>
        </ul>
        <label class="checkBtn" @click="display = !display">
          <div class="bar1"></div>
          <div class="bar2"></div>
          <div class="bar3"></div>
        </label>
      </nav>
    </header>

    <section>
      <div class="frontPage">
        <figure>
          <img
            class="frontImage"
            src="~@/assets/images/frontImg.jpg"
            alt="identity"
          />
        </figure>
        <div class="identity">
          <p class="name" v-for="(user, index) in myJson.info" :key="index">
            I am <strong>{{ user.name }}</strong>
          </p>
          <ul class="site">
            <li class="item">
              <a class="link" href="#">Facebook</a>
            </li>
            <li class="item">
              <a class="link" href="#">Twitter</a>
            </li>
            <li class="item">
              <a class="link" href="#">Linkedin</a>
            </li>
          </ul>
        </div>
      </div>
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
