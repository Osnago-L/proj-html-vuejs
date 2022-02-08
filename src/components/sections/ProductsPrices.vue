<template>
  <div class="products container">
      <div class="text">
        <h1 class="title">Find a freshly baked product perfect for you</h1>
        <p class="subtitle-p">Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis nemo similique soluta officiis.</p>
        <button class="button-purple">Start Shopping</button>
      </div>
      <div class="slideshow">
        <div class="arrow-left">&#8592;</div>
          <div class="img-container">      
              <img src="..\..\assets\img\choco-chip-cookies-600x765.jpg" alt="">
              <img src="..\..\assets\img\strawberry-jam-cookies-600x765.jpg" alt="">
              <img src="..\..\assets\img\strawberry-donut-600x765.jpg" alt="">
              <img src="..\..\assets\img\strawberry-donut-600x765.jpg" alt="">        
          </div>
        <div class="arrow-right">&#8594;</div>
      </div>
  </div>
</template>

<script>
export default {
    name: "ProductsPrices",
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
    display: flex;
    justify-content: end;

  .arrow-left,.arrow-right{
    position: absolute;
    top: 45%;
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
        
    width:100%;
    display: flex;
    gap: 15px;

    overflow-x: auto;

  img{
    width: 24%;
    object-fit: cover;
    object-position: center;
  }
}

}
</style>