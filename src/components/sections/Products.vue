<template>
  <div class="products container">
      <div class="text">
        <span>Our Products</span>
        <h1>All our delectable pastries are backed fresh in our Kitchen very morning, and are made with all-natural, all organic ingredients.</h1>
        <button class="button-purple">Start Shopping</button>
      </div>
      <div class="slideshow">
          <div class="img-container">
              <img src="..\..\assets\img\choco-chip-cookies-600x765.jpg" alt="">
              <img src="..\..\assets\img\strawberry-jam-cookies-600x765.jpg" alt="">
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: "Products",
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

  &>span{
    font-size: 13px;
    text-transform: uppercase;
    color: #929295;
    font-family: 'Roboto', sans-serif;
  }
  &>h1{
    font-size: 30px;
    color: $daisy-bush;
    margin-top: 15px;
    margin-bottom: 50px;
    font-family: 'Merriweather', serif;

  }

}
.slideshow{
    width: 60%;
    display: flex;
    justify-content: end;

    .img-container{
        width:100%;
        display: flex;
        gap: 15px;

    img{
        width: 50%;
        object-fit: cover;
        object-position: center;
    }
    }
    
}
</style>