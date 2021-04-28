<template>
  <div>
    <header>
      <nav class="container row space-between">
        <h2 class="logoName">Tawhid</h2>
        <ul class="nav-list">
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
        <label class="checkBtn" @click="myFunction">
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

    <section class="works">
      <article class="container">
        <header class="work-header">
          <h2>Awesome Works</h2>
          <p class="work-para">Check out latest works</p>
        </header>

        <div class="row wrap">
          <div
            class="col-33"
            v-for="(user, index) in myJson.images"
            :key="index"
          >
            <figure class="workColumn">
              <img
                class="workImg"
                :src="user.image"
                height="100%"
                width="100%"
              />
            </figure>
          </div>
        </div>
      </article>
    </section>

    <section class="connectWithUs">
      <article class="container">
        <header>
          <h2 class="contact-header">Get in Touch</h2>
          <p class="contact-para">
            Any question? Reach out to me and I will get back to you shortly.
          </p>
        </header>
        <div class="row justify-center">
          <div class="col-50">
            <form class="addForm">
              <input class="formName" type="text" placeholder="Your Name" />
              <input class="formEmail" type="text" placeholder="Your Email" />
              <textarea class="formText" placeholder="Your Message"></textarea>
            </form>
          </div>
        </div>
        <p class="button">
          <button class="submit">Send Message</button>
        </p>
      </article>
    </section>

    <footer>
      <section class="container">
        <p class="footer-para">
          © Copyright 2021. Template has been designed by Tawhid Sajib
        </p>
      </section>
    </footer>
  </div>
</template>
<script>
import user from "@/assets/json/user.json";
export default {
  data() {
    return {
      myJson: user,
    };
  },
  // mounted() {
  //   fetch("user.json")
  //     .then((res) => {
  //       return res.json();
  //     })
  //     .then((data) => {
  //       let serviceColumn = document.querySelectorAll(".serviceColumn");
  //       data.data.forEach((user, index) => {
  //         serviceColumn[index].innerHTML += `
  //             <h1 class="service-header">${user.header}</h1>
  //             <p class="service-para">${user.paragraph}</p>

  //             `;
  //       });

  //       let workColumn = document.querySelectorAll(".workColumn");
  //       data.images.forEach((user, index) => {
  //         workColumn[
  //           index
  //         ].innerHTML += `<img class="workImg" src="${user.image}" height="100%" width="100%">`;
  //       });

  //       let name = document.querySelector(".name");
  //       let phone = document.querySelector(".phone");
  //       let email = document.querySelector(".email");
  //       data.info.forEach((user) => {
  //         name.innerHTML += `I am <strong>${user.name}</strong>`;
  //         phone.innerHTML += `<span>Phone:</span> ${user.phone} `;
  //         email.innerHTML += `<span>Email:</span> ${user.email} `;
  //       });

  //       let skillName = document.querySelectorAll(".skillName");
  //       let skill = document.querySelectorAll(".skill");
  //       data.skills.forEach((user, index) => {
  //         skillName[index].innerHTML += `${user.name}`;
  //         skill[index].innerHTML += `${user.progress}`;
  //       });
  //     });
  // },
  methods: {
    myFunction() {
      var x = document.querySelector(".nav-list");
      if (x.style.display === "block") {
        x.style.display = "none";
      } else {
        x.style.display = "block";
      }
    },
    // getImage(path) {
    //   return require(path);
    // },
  },
};
</script>