<template>
  <div class="deals py-3">
    <div class="row max-width">
      <div class="col p-0">
        <hr />
      </div>
      <div class="col-2 p-0">
        <h1>Best Sellers</h1>
        <sub class="fs-5">Must have products from our top sellers</sub>
      </div>
      <div class="col p-0">
        <hr />
      </div>
    </div>

    <CardBox :selectedList="genericClothingList" />
  </div>
</template>

<script>
import CardBox from "./CardBox.vue";

export default {
  name: "BestSellerSection",
  components: {
    CardBox,
  },
  props: ["genericClothingList"],
};
</script>

<style scoped lang='scss'>
.deals {
  min-height: 600px;
}
</style>