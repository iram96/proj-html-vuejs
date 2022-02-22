<template>
  <div class="row justify-content-between div-border container-app">
    <div class="col-3 text-center">
      <div class="row mt-3">
        <div class="col-1"><i class="fa-brands fa-facebook-f"></i></div>
        <div class="col-1"><i class="fa-brands fa-twitter"></i></div>
        <div class="col-1"><i class="fa-brands fa-instagram"></i></div>
        <div class="col-1"><i class="fa-brands fa-youtube"></i></div>
      </div>
    </div>
    <div class="col-3 text-center">
      <header class="p-3 text-white">
        <div class="container">
          <div
            class="
              d-flex
              flex-wrap
              align-items-center
              justify-content-center justify-content-lg-start
            "
          >
            <form class="col-12 col-lg-auto mb-3 mb-lg-0 me-lg-3">
              <input
                type="search"
                class="form-control"
                placeholder="Search..."
                aria-label="Search"
              />
            </form>
          </div>
        </div>
      </header>
    </div>
  </div>
</template>

<script>
export default {
  name: "Techbar",
};
</script>

<style scoped lang='scss'>
</style>