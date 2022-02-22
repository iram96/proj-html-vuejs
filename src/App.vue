<template>
  <div id="app">
    <div>
      <Header />
      <Main :menJacketsList="menJacketsList" :seasonsList="seasonsList" />
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
      // ! ARRAY GIACCHE UOMO
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
          name: "Modern Black Leather Suit",
          tags: ["Men", "Jackets"],
          price: "$176",
          img: require("@/assets/img/modern_black_leather_suit-400x520.jpg"),
        },
      ],

      // ! ARRAY STAGIONI
      seasonsList: [
        {
          name: "Winter Collection",
          subTitle: "STYLISH AND WARM",
          img: require("@/assets/img/winter_collection_bg.jpg"),
        },
        {
          name: "Spring Collection",
          subTitle: "BRIGHT AND COLORFUL",
          img: require("@/assets/img/spring_collection_bg.jpg"),
        },
        {
          name: "Autumn Collection",
          subTitle: "RICH AND COMFORTABLE",
          img: require("@/assets/img/autumn_collection_bg.jpg"),
        },
      ],
    };
  },
  methods: {},
};
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap.scss";
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
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

    img {
      max-width: 100%;
    }
    .clearfix:after {
      display: table;
      content: "";
      clear: both;
    }
    .max-width {
      max-width: 100%;
    }
    .w-100 {
      width: 100%;
    }
  }
}
</style>
