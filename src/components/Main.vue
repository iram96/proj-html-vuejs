<template>
  <div id="main">
    <div class="imgs-section">
      <Jumbotron />
    </div>
    <ProductsSection :men_jackets_list="menJacketsList" />
    <div class="imgs-section">
      <div class="row">
        <div class="col"></div>
        <div class="col"></div>
        <div class="col"></div>
      </div>
    </div>
    <ProductsSection />
  </div>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import ProductsSection from "./ProductsSection.vue";

export default {
  name: "Main",
  props: ["menJacketsList"],
  components: {
    Jumbotron,
    ProductsSection,
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