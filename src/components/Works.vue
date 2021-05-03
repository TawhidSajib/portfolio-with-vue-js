<template>
  <div>
    <section class="works">
      <article class="container">
        <header class="work-header">
          <h2>Awesome Works</h2>
          <p class="work-para">Check out latest works</p>
        </header>

        <div class="row wrap">
          <div class="col-33" v-for="(image, index) in images" :key="index">
            <figure class="workColumn">
              <img class="workImg" :src="image" height="100%" width="100%" />
            </figure>
          </div>
        </div>
      </article>
    </section>
  </div>
</template>
<script>
import image1 from "@/assets/images/work1.jpg";
import image2 from "@/assets/images/work2.jpg";
import image3 from "@/assets/images/work3.jpg";
import image4 from "@/assets/images/work4.jpg";
import image5 from "@/assets/images/work5.jpg";
import image6 from "@/assets/images/work6.jpg";
export default {
  data() {
    return {
      images: [image1, image2, image3, image4, image5, image6],
    };
  },
};
</script>