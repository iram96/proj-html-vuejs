<template>
  <div id="app">
    <div>
      <Header />
      <Main
        :menJacketsList="menJacketsList"
        :seasonsList="seasonsList"
        :genericClothingList="genericClothingList"
        :femaleClothingList="femaleClothingList"
      />
      <Footer :seasonsList="seasonsList" />
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
      genericClothingList: [],
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
          tags: ["Jackets", "Men"],
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
      // ! ARRAY FEMMINILE
      femaleClothingList: [
        {
          name: "Hipster Black Top",
          tags: ["Women", "T-shirt"],
          price: "$57",
          img: require("@/assets/img/hipster_black_top-400x520.jpg"),
        },
        {
          name: "Spring Printed Dress",
          tags: ["Women", "Dress"],
          price: "$47",
          img: require("@/assets/img/spring_printed_dress-400x520.jpg"),
        },
        {
          name: "Modern Love Tee",
          tags: ["Women", "T-shirt"],
          price: "$68",
          img: require("@/assets/img/modern_love_tee-400x520.jpg"),
        },
        {
          name: "Black Jacket",
          tags: ["Women", "Jackets"],
          price: "$125",
          img: require("@/assets/img/black_leather_jacket-400x520.jpg"),
        },
      ],
    };
  },
  methods: {
    createList(firstArray, secondArray) {
      this.genericClothingList = firstArray.concat(secondArray);
    },
  },
  mounted() {
    this.createList(this.menJacketsList, this.femaleClothingList);
  },
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
      max-width: 70vw;
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
    .bg-transparent {
      border-color: white;
      border-width: 2px 2px 2px 2px;
      border-radius: 25px 25px 25px 25px;
      background: rgba(255, 255, 255, 0.114582);
      color: white;
    }
  }
}
</style>
