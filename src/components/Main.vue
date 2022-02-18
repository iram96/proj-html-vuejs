<template>
  <div>
    <Jumbotron />
    <ProductsSection />
  </div>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import ProductsSection from "./ProductsSection.vue";

export default {
  name: "Main",
  components: {
    Jumbotron,
    ProductsSection,
  },
};
</script>

<style>
</style>