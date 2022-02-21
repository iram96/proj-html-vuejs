<template>
  <div class="col">
    <div class="row div-border header-style"><TechBar /></div>
    <div class="row div-border header-style"><ShopBar /></div>
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
.header-style {
  max-width: 100%;
}
</style>