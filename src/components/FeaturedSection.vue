<template>
  <div id="section" class="div-border">
    <div class="container-app div-border">
      <div class="row">
        <div class="col">
          <hr />
        </div>
        <div class="col-2">
          <h4>Featured Products</h4>
          <sub>Must have products from our top sellers</sub>
        </div>
        <div class="col">
          <hr />
        </div>
      </div>
      <img src="..\assets\img\hover-button3.png" alt="" />
      <CardBox :menJacketsList="menJacketsList" class="" />
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
  min-height: 80vh;
}
</style>