<template>
  <div id="deals" class="div-border deals">
    <div class="row">
      <div class="col p-0">
        <hr />
      </div>
      <div class="col-2 p-0">
        <h4>Best Sellers</h4>
        <sub>Must have products from our top sellers</sub>
      </div>
      <div class="col p-0">
        <hr />
      </div>
    </div>

    <CardBox :menJacketsList="menJacketsList" />
  </div>
</template>

<script>
import CardBox from "./CardBox.vue";

export default {
  name: "BestSellerSection",
  components: {
    CardBox,
  },
  props: ["menJacketsList"],
};
</script>

<style scoped lang='scss'>
.deals {
  height: 600px;
}
</style>