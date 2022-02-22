<template>
  <div class="row max-width">
    <div class="container-app row">
      <div class="col-2 mx-0">
        <img :src="require('@/assets/img/classic_shop_logo1x.png')" alt="" />
      </div>
      <div class="col">
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
          <div class="container-fluid">
            <div
              class="collapse navbar-collapse justify-content-center"
              id="navbarNavDarkDropdown"
            >
              <ul class="navbar-nav row justify-content-end">
                <li
                  v-for="(item, index) in navbarList"
                  :key="index"
                  class="nav-item dropdown col"
                >
                  <a
                    class="nav-link dropdown-toggle"
                    href="#"
                    id="navbarDarkDropdownMenuLink"
                    role="button"
                    data-bs-toggle="dropdown"
                    aria-expanded="false"
                  >
                    {{ item }}
                  </a>
                  <ul
                    class="dropdown-menu dropdown-menu-dark"
                    aria-labelledby="navbarDarkDropdownMenuLink"
                  >
                    <li><a class="dropdown-item" href="#">Action</a></li>
                    <li>
                      <a class="dropdown-item" href="#">Another action</a>
                    </li>
                    <li>
                      <a class="dropdown-item" href="#">Something else here</a>
                    </li>
                  </ul>
                </li>
                <li class="nav-item dropdown col">
                  <button type="button" class="btn btn-primary rounded-pill">
                    Primary
                  </button>
                </li>
              </ul>
            </div>
          </div>
        </nav>
      </div>
      <div class="col-2">
        <i class="fa-solid fa-user"></i>
        <i class="fa-solid fa-bag-shopping"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ShopBar",
  props: ["navbarList"],
};
</script>

<style scoped lang='scss'>
</style>