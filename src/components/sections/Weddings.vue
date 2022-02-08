<template>
  <div class="weddings container">
      <span class="title-header">Corporate & Weddings</span>
      <h1 class="title">Baking Special Moment</h1>
      <div class="wedding-images">
          <div><img src="..\..\assets\img\corporate-bg.jpg" alt=""></div>
          <div><img src="..\..\assets\img\wedding-bg.jpg" alt=""></div>  
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
    
    .wedding-images{
        padding-top: 40px;
        display: flex;
        gap: 80px;

        &>div{
            width: 50%;
        }

        img{
           width: 100%;
           object-fit: cover;
        }
    }
}
</style>