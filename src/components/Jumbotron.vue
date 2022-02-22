<template>
  <div id="jumbotron" class="position-relative">
    <div class="position-absolute top-50 start-50 translate-middle">
      <h1 class="fw-bold title">Brand New Arrivals</h1>
      <p class="fs-2">View Collection from New York</p>
      <button type="button" class="btn bg-transparent rounded-pill">
        View more
      </button>
      <button type="button" class="btn bg-transparent rounded-pill">
        Lookbook
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Jumbotron",
};
</script>

<style scoped lang='scss'>
#jumbotron {
  min-height: inherit;
  background-image: url("../assets/img/home1_slide_three_bg_2.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  background-attachment: scroll;
  color: white;
  .title {
    font-size: 6em;
  }
}
</style>