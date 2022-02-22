<template>
  <div class="col-2">
    <img :src="item.img" alt="" class="featured-img d-block w-100" />
    <span class="d-block">{{ item.name }}</span>
    <div class="d-block">
      <span v-for="tag in item.tags" :key="tag.name"> {{ tag }}</span>
    </div>
    <span class="d-block">{{ item.price }}</span>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["item"],
};
</script>

<style scoped lang='scss'>
</style>