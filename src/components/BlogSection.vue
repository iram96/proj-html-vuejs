<template>
  <div id="blog">
    <div class="row max-width">
      <div class="col p-0">
        <hr />
      </div>
      <div class="col-2 p-0">
        <h4>Best Sellers</h4>
        <sub>Must have products from our top sellers</sub>
      </div>
      <div class="col p-0">
        <hr />
      </div>
    </div>
    <div class="row justify-content-center max-width">
      <div class="col-3 text-start">
        <img
          :src="require('@/assets/img/post_img_12-320x202.jpg')"
          alt=""
          class="d-block w-100"
        />
        <h3>Title</h3>
        <span>subtitle</span>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempore
          cupiditate repellendus libero repellat totam sequi dignissimos
          repudiandae. Et optio mollitia dicta vitae nihil minima hic id animi
          consectetur. Fugit, deleniti.
        </p>
      </div>
      <div class="col-3 text-start">
        <img
          :src="require('@/assets/img/post_img_11-320x202.jpg')"
          alt=""
          class="d-block w-100"
        />
        <h3>Title</h3>
        <span>subtitle</span>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempore
          cupiditate repellendus libero repellat totam sequi dignissimos
          repudiandae. Et optio mollitia dicta vitae nihil minima hic id animi
          consectetur. Fugit, deleniti.
        </p>
      </div>
      <div class="col-3 text-start">
        <img
          :src="require('@/assets/img/post_img_10-320x202.jpg')"
          alt=""
          class="d-block w-100"
        />
        <h3>Title</h3>
        <span>subtitle</span>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempore
          cupiditate repellendus libero repellat totam sequi dignissimos
          repudiandae. Et optio mollitia dicta vitae nihil minima hic id animi
          consectetur. Fugit, deleniti.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BlogSection",
};
</script>

<style scope lang='scss'>
#blog {
  min-height: 600px;
}
</style>