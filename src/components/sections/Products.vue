<template>
  <div class="products container">
    <div class="text">
      <span class="title-header">Our Products</span>
      <h1 class="title">
        All our delectable pastries are backed fresh in our Kitchen very
        morning, and are made with all-natural, all organic ingredients.
      </h1>
      <button class="button-purple">Start Shopping</button>
    </div>
    <div class="slideshow">
      <div @click="slidebackward" class="arrow-left">&#8592;</div>
      <div @click="slideForward" class="arrow-right">&#8594;</div>
      <div class="img-container">
        <div v-for="(element, index) in items" :key="index">
          <img
            @mouseover="mouseOverProducts"
            class="product-image"
            :src="element.img"
            alt=""
          />
          <div
            @mouseleave="mouseOutProducts"
            class="products-info display-none"
          >
            <h1 class="title">{{ element.name }}</h1>
            <span class="subtitle-p">{{ element.category.join(", ") }}</span>
            <span class="title-header">{{ element.price }}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { productsList } from "../../assets/javascript/data";
export default {
  name: "Products",
  data() {
    return {
      items: [],
    };
  },
  methods: {
    slideForward(event) {
      console.log(event);
      let imgWidth = event.path[1].querySelector(".product-image").width;
      event.path[1].querySelector(".img-container").scrollLeft += imgWidth + 15;
    },
    slidebackward(event) {
      let imgWidth = event.path[1].querySelector(".product-image").width;
      event.path[1].querySelector(".img-container").scrollLeft -= imgWidth + 15;
    },
    mouseOverProducts(event) {
      event.path[1]
        .querySelector(".products-info")
        .classList.remove("display-none");
    },
    mouseOutProducts(event) {
      event.path[1]
        .querySelector(".products-info")
        .classList.add("display-none");
    },
  },
  created() {
    this.items = productsList;
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partial/variables.scss";
.products {
  padding-top: 140px;
  display: flex;
  justify-content: space-between;
}
.text {
  width: 30%;
  margin-right: 60px;
}
.slideshow {
  position: relative;
  width: 60%;
  display: flex;
  justify-content: end;

  .arrow-left,
  .arrow-right {
    position: absolute;
    top: 45%;
    z-index: 999;
    height: 80px;
    width: 40px;
    background-color: $daisy-bush;
    opacity: 0.5;
    color: white;
    cursor: pointer;

    display: flex;
    align-items: center;
    justify-content: center;
  }
  .arrow-right {
    right: 0;
  }
  .arrow-left {
    left: 0;
  }

  .img-container {
    width: 100%;
    display: flex;
    gap: 15px;
    overflow-x: auto;

    & > div {
      position: relative;
      width: 50%;
      display: flex;
      flex: 0 0 auto;
    }

    img {
      width: 100%;
      object-fit: cover;
      object-position: center;
    }
  }
  .products-info {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(black, 0.164);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    h1,
    span {
      color: white;
    }
    span.title-header {
      font-size: 20px;
    }
    span.subtitle-p {
      font-size: 14px;
    }
  }
}
</style>