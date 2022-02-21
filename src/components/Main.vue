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
  </div>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import FeaturedSection from "./FeaturedSection.vue";
import BestSellerSection from "./BestSellerSection.vue";
import SeasonsCard from "./SeasonsCard.vue";

export default {
  name: "Main",
  props: ["menJacketsList", "seasonsList"],
  components: {
    Jumbotron,
    FeaturedSection,
    BestSellerSection,
    SeasonsCard,
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
}
</style>