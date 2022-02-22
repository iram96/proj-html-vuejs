<template>
  <div id="footer">
    <section id="email-submit">
      <div class="container-app"></div>
    </section>
    <section id="shopping-info"></section>
    <section id="end-page"></section>
  </div>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped lang='scss'>
#footer {
  #email-submit {
    background-color: #2e3238;
    min-height: 150px;
  }
  #shopping-info {
    background-color: #2b2e32;
    min-height: 300px;
  }
  #end-page {
    background-color: #1c1e21;
    min-height: 100px;
  }
}
</style>