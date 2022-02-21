<template>
  <div id="app">
    <div>
      <Header />
      <Main :men_jackets_list="menJacketsList" />
      <Footer />
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return {
      menJacketsList: [
        {
          name: "Black Leather Jacket",
          tags: ["Men", "Jackets", "Jeans"],
          price: "$200",
          img: require("@/assets/img/black_elegant_leather_jacket-200x260.jpg"),
        },
        {
          name: "Black Leather Suit",
          tags: ["Men", "Jackets"],
          price: "$176",
          img: require("@/assets/img/black_leather_suit-400x520.jpg"),
        },
        {
          name: "Blue Jacket and White Tee",
          tags: ["Men", "Jackets", "Suits"],
          price: "$176",
          img: require("@/assets/img/blue_jacket_and_white_stripe_tee-400x520.jpg"),
        },
        {
          name: "Black Leather Suit",
          tags: ["Men", "Jackets"],
          price: "$176",
          img: require("@/assets/img/modern_black_leather_suit-400x520.jpg"),
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap.scss";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  .container-app {
    max-width: 80vw;
    margin: 0 auto;
  }
  .div-border {
    border: black dotted 3px;
  }
}
</style>
