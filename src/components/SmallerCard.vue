<template>
  <div id="card " class="row">
    <div class="d-inline-block col">
      <span class="d-block">{{ item.name }}</span>
      <span>{{ item.subTitle }}</span>
    </div>
    <div class="col-3">
      <img :src="item.img" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "SmallerCard",
  props: ["item"],
};
</script>

<style scoped lang='scss'>
#card {
  border-bottom: 2px black solid;
  img {
    width: 30px;
    height: 60px;
    display: inline-block;
  }
}
</style>