<template>
  <div>
    <section class="container">
      <section class="row">
        <div class="col-25">
          <div>
            <figure>
              <img class="myself" src="~@/assets/images/me.jpeg" alt="me" />
            </figure>
          </div>
        </div>

        <div class="col-75">
          <div class="aboutColumn">
            <h2 class="aboutHeader">About Me</h2>
            <h3 class="describe">i'm front end web developer</h3>
            <p class="definition">
              Tawhid is a Resume perfectly for Professional
              Portfolio,designers,<br />
              developers,coders or any other profession. I'm very passionate and
              <br />
              dedicated to my work.
            </p>
            <div
              class="skills-type"
              v-for="(user, index) in myJson.skills"
              :key="index"
            >
              <h4 class="skillName">{{ user.name }}</h4>
              <p class="skill html-progress">{{ user.progress }}</p>
            </div>
            <div
              class="contact"
              v-for="(user, index) in myJson.info"
              :key="index"
            >
              <p class="phone">Phone: {{ user.name }}</p>
              <br />
              <p class="email">Email: {{ user.phone }}</p>
            </div>
            <div><button class="cvBtn">Download cv</button></div>
          </div>
        </div>
      </section>
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