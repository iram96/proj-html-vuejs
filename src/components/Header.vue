<template>
  <div class="col">
    <div class="row div-border"><TechBar /></div>
    <div class="row div-border"><ShopBar /></div>
  </div>
</template>

<script>
import TechBar from "./TechBar.vue";
import ShopBar from "./ShopBar.vue";

export default {
  name: "Header",
  components: {
    TechBar,
    ShopBar,
  },
};
</script>

<style scoped lang='scss'>
</style>