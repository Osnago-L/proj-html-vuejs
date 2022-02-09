<template>
  <div class="products container">
      <div class="text">
        <h1 class="title">Find a freshly baked product perfect for you</h1>
        <p class="subtitle-p">Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis nemo similique soluta officiis.</p>
        <button class="button-purple">Start Shopping</button>
      </div>
      <div class="slideshow">
        <div @click="slidebackward" class="arrow-left">&#8592;</div>
        <div @click="slideForward" class="arrow-right">&#8594;</div>
          <div class="img-container">     
            <div v-for="element,index in items" :key="index">
                <img class="product-image" :src="element.img" alt="">
                <span class="name">{{element.name}}</span>
                <span class="price">{{element.price}}</span>
            </div>
          </div>

      </div>
  </div>
</template>

<script>
import {productsList} from "../../assets/javascript/data";
export default {
    name: "ProductsPrices",
    data(){
      return{
        items:[]
      }
    },
    methods:{
      slideForward(event){
        let imgWidth =  event.path[1].querySelector(".product-image").width;
        event.path[1].querySelector(".img-container").scrollLeft += (imgWidth + 15)
      },
      slidebackward(event){
        let imgWidth =  event.path[1].querySelector(".product-image").width;
        event.path[1].querySelector(".img-container").scrollLeft -= (imgWidth + 15)
      },
    },
    created(){
      this.items = productsList
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/partial/variables.scss";
.products{
    padding-top: 140px;
    display: flex;
    justify-content: space-between;
}
.text{
  width: 30%;
  margin-right: 60px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.slideshow{
    position: relative;
    width: 60%;

  .arrow-left,.arrow-right{
    position: absolute;
    top: 40%;
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
  .arrow-right{
    right: 0;
  }
  .arrow-left{
    left: 0;
  }

  .img-container{
    position: relative;
    width:100%;
    height: 100%;
    display: flex;
    gap: 15px;

    overflow: auto;

    &>div{
      width: 24.2%;
      display: flex;
      flex-direction: column;
      align-items: center;
      flex: 0 0 auto;

      img{
        width: 100%;
        object-fit: cover;
        object-position: center;
      }
      .name{
        margin: 8px 0;
        color: $daisy-bush;
        font-size: 16px;
        font-family: 'Merriweather', serif;
        font-weight: 900;
      }
      .price{
        font-size: 14px;
        color: #929295;
        font-family: 'Roboto', sans-serif;
      }
    }
  }
}
</style>