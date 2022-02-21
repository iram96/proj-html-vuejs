<template>
  <div
    class="col season-card"
    :style="{ 'background-image': `url(${season.img})` }"
  ></div>
</template>

<script>
export default {
  name: "SeasonsCard",
  props: ["season"],
};
</script>

<style scoped lang='scss'>
.imgs-section {
  width: 100%;
  margin: 0;
}
.season-card {
  height: 65vh;
  background-size: cover;
  background-repeat: no-repeat;
}
</style>