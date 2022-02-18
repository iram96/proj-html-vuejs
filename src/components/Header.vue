<template>
  <div>
    <TechBar />
    <ShopBar />
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

<style>
</style>