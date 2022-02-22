<template>
  <div id="footer">
    <section id="email-submit">
      <div class="container-app row py-5">
        <div class="col">
          <div class="row justify-content-start">
            <div class="circle col-1">
              <i
                class="
                  fas
                  fa-envelope
                  text-white
                  position-absolute
                  top-50
                  start-50
                  translate-middle
                "
              ></i>
            </div>
            <h4 class="d-inline col-8 text-white">
              Subscribe now and get special offer
            </h4>
          </div>
        </div>
        <div class="col-5">
          <div class="input-group mb-3">
            <input
              type="text"
              class="form-control"
              placeholder="Recipient's username"
              aria-label="Recipient's username"
              aria-describedby="button-addon2"
            />
            <button
              class="btn btn-outline-secondary"
              type="button"
              id="button-addon2"
            >
              Button
            </button>
          </div>
        </div>
      </div>
    </section>
    <section id="shopping-info">
      <div class="container-app row py-5">
        <div class="col infos text-white text-start">
          <img
            :src="require('@/assets/img/classic_shop_logo_footer.png')"
            alt=""
            class="max-width mb-3"
          />
          <span class="d-block">12345 North Main Street,</span>
          <span class="d-block">New York, NY 555555,</span>
          <span class="d-block">Phone: 1.800.555.6789</span>
          <span class="d-block">Email: info@company.com</span>
          <span class="d-block">Web: Theme-fusion.com</span>

          <div class="row mt-3">
            <div class="col-1"><i class="fa-brands fa-facebook-f"></i></div>
            <div class="col-1"><i class="fa-brands fa-twitter"></i></div>
            <div class="col-1"><i class="fa-brands fa-instagram"></i></div>
            <div class="col-1"><i class="fa-brands fa-youtube"></i></div>
          </div>
        </div>
        <div class="col text-white">
          <h5>TOP RATED PRODUCTS</h5>
          <SmallerCard
            v-for="item in seasonsList"
            :key="item.name"
            :item="item"
          />
        </div>
        <div class="col text-white">
          <h5>RECENT POSTS</h5>
          <ul>
            <li><a href="#">Aenean lobortis sapien enim viverra</a></li>
            <li><a href="#">Aenean lobortis sapien enim viverra</a></li>
            <li><a href="#">Aenean lobortis sapien enim viverra</a></li>
            <li><a href="#">Aenean lobortis sapien enim viverra</a></li>
            <li><a href="#">Aenean lobortis sapien enim viverra</a></li>
            <li><a href="#">Aenean lobortis sapien enim viverra</a></li>
            <li><a href="#">Aenean lobortis sapien enim viverra</a></li>
            <li><a href="#">Aenean lobortis sapien enim viverra</a></li>
          </ul>
        </div>
        <div class="col text-white">
          <h5>TAGS</h5>
          <div class="tagcloud">
            <a href="#">parola</a>
            <a href="#">ape</a>
            <a href="#">ciao</a>
            <a href="#">ape</a>
            <a href="#">parola</a>
            <a href="#">ciao</a>
            <a href="#">parola</a>
            <a href="#">ciao</a>
            <a href="#">parola</a>
            <a href="#">ape</a>
            <a href="#">ciao</a>
            <a href="#">parola</a>
            <a href="#">ape</a>
            <a href="#">parola</a>
            <a href="#">ciao</a>
            <a href="#">ape</a>
            <a href="#">parola</a>
          </div>
        </div>
      </div>
    </section>
    <section id="end-page"></section>
  </div>
</template>

<script>
import SmallerCard from "./SmallerCard.vue";
export default {
  name: "Footer",
  components: {
    SmallerCard,
  },
  props: ["seasonsList"],
};
</script>

<style scoped lang='scss'>
#footer {
  #email-submit {
    background-color: #2e3238;

    .circle {
      height: 30px;
      width: 30px;
      background-color: black;
      border-radius: 50%;
      position: relative;
    }
  }
  #shopping-info {
    background-color: #2b2e32;
    min-height: 300px;
    .infos {
      img {
        height: 50px;
      }
    }
    ul {
      list-style-type: none;
      li:before {
        font-family: "FontAwesome";
        content: "\f105";
        margin: 0 5px 0 -15px;
      }
      li {
        a {
          text-decoration: none;
          color: white;
        }
      }
    }
    .tagcloud {
      text-align: left;
      a {
        display: inline-flex;
        align-items: center;
        margin: 2px 0;
        padding: 0 10px;
        min-height: 2.15em;
        border: 1px solid;
        text-shadow: none;
        color: white;
        text-decoration: none;
      }
    }
  }
  #end-page {
    background-color: #1c1e21;
    min-height: 100px;
  }
}
</style>