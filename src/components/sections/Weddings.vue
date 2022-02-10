<template>
  <div class="weddings container">
    <span class="title-header">Corporate & Weddings</span>
    <h1 class="title">Baking Special Moment</h1>
    <div class="wedding-images">
      <div
        @mouseover="hoverOnImage(element)"
        @mouseleave="hoverLeaveImage(element)"
        v-for="(element, index) in item"
        :key="index"
      >
        <img :src="element.event ? element.imgHover : element.img" alt="" />
        <div class="image-info" v-show="element.event">
          <span class="title-header">Private & Dining Hall</span>
          <h1 class="title">Weddings & Parties</h1>
          <button class="button-purple">Explore More</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { corporateWedding } from "../../assets/javascript/data";
export default {
  name: "Weddings",
  data() {
    return {
      item: [],
    };
  },
  methods: {
    hoverOnImage(element) {
      console.log(element);
      element.event = true;
    },
    hoverLeaveImage(element) {
      console.log(element);
      element.event = false;
    },
  },
  created() {
    this.item = corporateWedding;
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partial/variables.scss";
.weddings {
  padding-top: 120px;
  text-align: center;

  .wedding-images {
    padding-top: 40px;
    display: flex;
    gap: 80px;

    & > div {
      position: relative;
      width: 50%;
    }

    img {
      width: 100%;
      object-fit: cover;
    }

    .image-info {
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
      z-index: 999;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;

      span.title-header {
        font-size: 14px;
        color: white;
      }

      h1.title {
        font-size: 40px;
        color: white;
      }
    }
  }
}
</style>