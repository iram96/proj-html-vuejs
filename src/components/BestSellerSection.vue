<template>
  <div>
    <div id="section" class="div-border">
      <div class="container-app div-border">
        <div class="row">
          <div class="col">
            <hr />
          </div>
          <div class="col-2">
            <h4>Best Sellers</h4>
            <sub>Must have products from our top sellers</sub>
          </div>
          <div class="col">
            <hr />
          </div>
        </div>

        <CardBox :menJacketsList="menJacketsList" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>