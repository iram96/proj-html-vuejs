<template>
  <div class="row justify-content-center max-width">
    <div class="container">
      <div class="row">
        <div class="col-3 d-flex align-items-center justify-content-center">
          <i class="fas fa-angle-left fa-4x" @click="nextImage()"></i>
        </div>
        <div class="col-6">
          <div class="slider d-flex align-items-center m-auto overflow-hidden">
            <Card v-for="item in selectedList" :key="item.name" :item="item" />
          </div>
        </div>
        <div class="col-3 d-flex align-items-center justify-content-center">
          <i class="fas fa-angle-right fa-4x" @click="prevImage()"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";
export default {
  name: "CardBox",
  props: ["selectedList"],
  components: {
    Card,
  },
  data() {
    return {
      currentId: 0,
    };
  },
  methods: {
    isActive(index) {
      return index === this.currentId;
    },
    nextImage() {
      if (this.currentId === this.images.length - 1) {
        return (this.currentId = 0);
      } else {
        return this.currentId++;
      }
    },
    prevImage() {
      if (this.currentId === 0) {
        return (this.currentId = this.images.length - 1);
      } else {
        return this.currentId--;
      }
    },
    getPicture(index) {
      this.currentId = index;
    },
  },
};
</script>

<style scoped>
.slider {
  height: 500px;
  position: relative;
  max-width: 500px;
  justify-content: center;
}

[class*="fa-angle"] {
  cursor: pointer;
}

.slider .slider-dots {
  background-color: rgba(0, 0, 0, 0.3);
  padding: 5px;
  border-radius: 20px;
  display: flex;
  position: absolute;
  top: 100%;
  left: 50%;

  transform: translateX(-50%);
}

.slider-dots .dot {
  height: 20px;
  width: 20px;
  border-radius: 50%;
  background-color: #fff;
  cursor: pointer;
}

.slider-dots .dot.active {
  background-color: dodgerblue;
}
</style>