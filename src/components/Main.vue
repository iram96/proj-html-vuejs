<template>
  <div id="main">
    <div class="imgs-section">
      <Jumbotron />
    </div>
    <FeaturedSection :menJacketsList="menJacketsList" />
    <div class="imgs-section">
      <div class="row">
        <div class="col"></div>
        <div class="col"></div>
        <div class="col"></div>
      </div>
    </div>
    <BestSellerSection />
  </div>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import FeaturedSection from "./FeaturedSection.vue";
import BestSellerSection from "./BestSellerSection.vue";

export default {
  name: "Main",
  props: ["menJacketsList"],
  components: {
    Jumbotron,
    FeaturedSection,
    BestSellerSection,
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
}
</style>