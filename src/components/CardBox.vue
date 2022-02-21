<template>
  <div class="row justify-content-center">
    <Card
      v-for="jacket in menJacketsList"
      :key="jacket.name"
      :jacket="jacket"
    />
  </div>
</template>

<script>
import Card from "./Card.vue";
export default {
  name: "CardBox",
  props: ["menJacketsList"],
  components: {
    Card,
  },
};
</script>

<style>
</style>