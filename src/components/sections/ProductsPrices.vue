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
            <div>
                <img src="..\..\assets\img\choco-chip-cookies-500x638.jpg" alt="">
                <span>Prezzo</span>
                <span>Prezzo</span>
            </div>
            <div><img src="..\..\assets\img\strawberry-jam-cookies-600x765.jpg" alt=""></div>
            <div><img src="..\..\assets\img\strawberry-donut-600x765.jpg" alt=""></div>
            <div><img src="..\..\assets\img\strawberry-donut-600x765.jpg" alt=""></div>
            <div><img src="..\..\assets\img\strawberry-donut-600x765.jpg" alt=""></div>       
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

  .arrow-left,.arrow-right{
    position: absolute;
    top: 40%;
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

    overflow: auto;

    &>div{
      width: 24%;
      height: 350px;
      display: flex;
      flex-direction: column;
      align-items: center;
      flex: 0 0 auto;
    }

  img{
    width: 100%;
    object-fit: cover;
    object-position: center;
  }
  }

}
</style>