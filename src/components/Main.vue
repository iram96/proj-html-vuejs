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
      <BestSellerSection :menJacketsList="menJacketsList" />
    </section>
    <section class="bg-style" id="deals-section">
      <div class="container-app div-border row justify-content-around">
        <div class="col-4">
          <img src="..\assets\img\promo_box_1_bg.jpg" alt="" />
        </div>
        <div class="col-4">
          <img src="..\assets\img\promo_box_2_bg.jpg" alt="" />
        </div>
      </div>
    </section>
    <BestSellerSection :menJacketsList="menJacketsList" />
    <section
      id="reviews"
      :style="{ 'background-image': `url(${reviewImg})` }"
    ></section>
    <section id="blog">
      <BlogSection />
      <hr />
    </section>
    <section id="categories" class="row justify-content-center max-width">
      <div class="col-2">
        <SmallerCard
          v-for="item in seasonsList"
          :key="item.name"
          :item="item"
        />
      </div>

      <div class="col-2">
        <SmallerCard
          v-for="item in seasonsList"
          :key="item.name"
          :item="item"
        />
      </div>

      <div class="col-2">
        <SmallerCard
          v-for="item in seasonsList"
          :key="item.name"
          :item="item"
        />
      </div>

      <div class="col-2">
        <SmallerCard
          v-for="item in seasonsList"
          :key="item.name"
          :item="item"
        />
      </div>
    </section>
    <section id="brand-logos" class="text-center">
      <h4>Brand Logos</h4>
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

export default {
  name: "Main",
  props: ["menJacketsList", "seasonsList"],
  components: {
    Jumbotron,
    FeaturedSection,
    BestSellerSection,
    SeasonsCard,
    BlogSection,
    SmallerCard,
  },
  data() {
    return {
      reviewImg: require("@/assets/img/testimonials_home_1_bg.jpg"),
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
    background-color: #f4f8f9;
  }
  #reviews {
    min-height: 60vh;
    background-attachment: fixed;
  }
  #brand-logos {
    min-height: 300px;
    background-color: #f6f6f6;
  }
}
</style>