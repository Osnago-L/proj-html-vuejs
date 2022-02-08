<template>
  <div class="products container">
      <div class="text">
        <span>Our Products</span>
        <h1 class="title">All our delectable pastries are backed fresh in our Kitchen very morning, and are made with all-natural, all organic ingredients.</h1>
        <button>Explore our products</button>
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
    height: 750px;
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
  &>.title{
    font-size: 30px;
    color: $daisy-bush;
    margin-top: 15px;
    margin-bottom: 50px;
    font-family: 'Merriweather', serif;

  }
  &>button{
    border: none;
    border-radius: 6px 6px;
    background-color: $daisy-bush;
    padding: 10px 30px;
    font-size: 14px;
    font-family: 'Roboto', sans-serif;
    color: white;
    cursor: pointer;
  }
}
.slideshow{
    width: 60%;
    display: flex;
    justify-content: end;
    border: 1px solid black;

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