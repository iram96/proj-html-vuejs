<template>
  <div>
    <img :src="jacket.img" alt="" class="featured-img" />
    <span>{{ jacket.name }}</span>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["jacket"],
};
</script>

<style scoped lang='scss'>
.featured-img {
  width: 100px;
  height: 200px;
}
</style>