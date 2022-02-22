<template>
  <div id="section" class="py-3">
    <div class="container-app div-border w-100">
      <div class="row max-width">
        <div class="col p-0">
          <hr />
        </div>
        <div class="col-4">
          <h1>Featured Products</h1>
          <sub class="fs-5">Must have products from our top sellers</sub>
        </div>
        <div class="col p-0">
          <hr />
        </div>
      </div>
      <img src="..\assets\img\hover-button3.png" alt="" />
      <CardBox :selectedList="menJacketsList" class="" />
    </div>
  </div>
</template>

<script>
import CardBox from "./CardBox.vue";
export default {
  name: "ProductsSection",
  props: ["menJacketsList"],
  components: {
    CardBox,
  },
};
</script>

<style scoped lang='scss'>
#section {
  .w-100 {
    height: 70vh;
  }
}
</style>