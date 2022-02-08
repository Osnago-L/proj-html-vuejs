<template>
  <div class="weddings container">
      <span>Corporate & Weddings</span>
      <h1>Baking Special Moment</h1>
      <div class="wedding-images">
          <img src="..\..\assets\img\corporate-bg.jpg" alt="">
          <img src="..\..\assets\img\wedding-bg.jpg" alt="">
      </div>
  </div>
</template>

<script>
export default {
    name: "Weddings"
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/partial/variables.scss";
.weddings{
    padding-top: 120px;
    text-align: center;

    &>span{
    font-size: 13px;
    text-transform: uppercase;
    color: #929295;
    font-family: 'Roboto', sans-serif;
    }

    &>h1{
    font-size: 30px;
    color: $daisy-bush;
    margin-top: 10px;
    margin-bottom: 50px;
    font-family: 'Merriweather', serif;
    }
    
    .wedding-images{
        display: flex;
        gap: 20px;
        
        img{
            width: 50%;
        }
    }
}


</style>