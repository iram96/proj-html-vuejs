<template>
  <div id="main">
    <section class="imgs-section">
      <Jumbotron />
    </section>
    <FeaturedSection :menJacketsList="menJacketsList" />
    <section class="imgs-section row m-0" id="season-cards">
      <SeasonsCard
        v-for="season in seasonsList"
        :key="season.name"
        :season="season"
      />
    </section>
    <section class="container-app div-border" id="best-sellers">
      <BestSellerSection :genericClothingList="genericClothingList" />
    </section>
    <section class="bg-style" id="deals-section">
      <div class="container-app row justify-content-around">
        <div class="col-4 my-4 promo1 text-white p-5 text-start">
          <h4>70% OFF</h4>
          <p>Vivamus tempor leo lacus, feugiat ut magna aliquam erat.</p>
          <button type="button" class="btn bg-transparent rounded-pill">
            View more
          </button>
        </div>
        <div class="col-4 my-4 promo2 text-white p-5 text-start">
          <h4>FREE SHIPPING</h4>
          <p>Vivamus tempor leo lacus, feugiat ut magna aliquam erat.</p>
          <button type="button" class="btn bg-transparent rounded-pill">
            View more
          </button>
        </div>
      </div>
    </section>
    <NewArrivalsSection :genericClothingList="genericClothingList" />
    <section
      id="reviews"
      :style="{ 'background-image': `url(${reviewImg})` }"
      class="position-relative"
    >
      <div
        class="position-absolute top-50 start-50 translate-middle text-white"
      >
        <img :src="require('@/assets/img/man_testimonial.png')" alt="" />
        <p class="my-3">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Delectus
          doloremque natus quaerat expedita ipsa neque unde earum autem vel
          reiciendis ab, hic fuga et incidunt. Quam soluta eum repellat
          doloribus.
        </p>
      </div>
    </section>
    <section id="blog">
      <BlogSection />
      <hr />
    </section>
    <section
      id="categories"
      class="row justify-content-center max-width overflow-hidden"
    >
      <div class="col-2">
        <h4>FEATURED</h4>
        <SmallerCard
          v-for="item in genericClothingList"
          :key="item.name"
          :item="item"
        />
      </div>

      <div class="col-2">
        <h4>ON SALE</h4>
        <SmallerCard
          v-for="item in seasonsList"
          :key="item.name"
          :item="item"
        />
      </div>

      <div class="col-2">
        <h4>TOP RATED</h4>
        <SmallerCard
          v-for="item in femaleClothingList"
          :key="item.name"
          :item="item"
        />
      </div>

      <div class="col-2">
        <h4>LATEST REVIEW</h4>
        <SmallerCard
          v-for="item in seasonsList"
          :key="item.name"
          :item="item"
        />
      </div>
    </section>
    <section id="brand-logos" class="text-center">
      <h4 class="py-3">Brand Logos</h4>
      <img
        v-for="logo in brandLogos"
        :key="logo.name"
        :src="logo.img"
        alt=""
        class="mx-3"
      />
    </section>
  </div>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import FeaturedSection from "./FeaturedSection.vue";
import BestSellerSection from "./BestSellerSection.vue";
import SeasonsCard from "./SeasonsCard.vue";
import BlogSection from "./BlogSection.vue";
import SmallerCard from "./SmallerCard.vue";
import NewArrivalsSection from "./NewArrivalsSection.vue";

export default {
  name: "Main",
  props: [
    "menJacketsList",
    "seasonsList",
    "genericClothingList",
    "femaleClothingList",
  ],
  components: {
    Jumbotron,
    FeaturedSection,
    BestSellerSection,
    SeasonsCard,
    BlogSection,
    SmallerCard,
    NewArrivalsSection,
  },
  data() {
    return {
      reviewImg: require("@/assets/img/testimonials_home_1_bg.jpg"),
      brandLogos: [
        {
          name: "Forest",
          img: require("@/assets/img/b_logotype_1.png"),
        },
        {
          name: "Badge",
          img: require("@/assets/img/b_logotype_2.png"),
        },
        {
          name: "Beard Fashion",
          img: require("@/assets/img/b_logotype_3.png"),
        },
        {
          name: "Hype",
          img: require("@/assets/img/b_logotype_4.png"),
        },
        {
          name: "A&Q",
          img: require("@/assets/img/b_logotype_5.png"),
        },
        {
          name: "Authentic",
          img: require("@/assets/img/b_logotype_6.png"),
        },
        {
          name: "The Yard",
          img: require("@/assets/img/b_logotype_7.png"),
        },
      ],
    };
  },
};
</script>

<style scoped lang='scss'>
#main {
  max-width: 100%;
  .imgs-section {
    width: 100%;
    min-height: 700px;
  }
  .bg-style {
    background-image: url("../assets/img/bkgd_confetti-compressor.jpg");
    background-position: center;
    .promo1 {
      background-image: url("../assets/img/promo_box_1_bg.jpg");
      background-size: contain;
      background-repeat: no-repeat;
      min-height: 300px;
    }
    .promo2 {
      background-image: url("../assets/img/promo_box_2_bg.jpg");
      background-size: contain;
      background-repeat: no-repeat;
      min-height: 300px;
    }
  }
  #reviews {
    min-height: 60vh;
    background-attachment: fixed;
  }
  #brand-logos {
    min-height: 300px;
    background-color: #f6f6f6;
  }
  #categories {
    max-height: 320px;
  }
}
</style>