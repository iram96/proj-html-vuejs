<template>
  <div
    class="col season-card text-white position-relative"
    :style="{ 'background-image': `url(${season.img})` }"
  >
    <div class="position-absolute bottom-0 start-50 translate-middle-x mb-4">
      <h4 class="fs-1">{{ season.name }}</h4>
      <p>{{ season.subTitle }}</p>
      <button type="button" class="btn bg-transparent rounded-pill">
        View more
      </button>
    </div>
  </div>
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