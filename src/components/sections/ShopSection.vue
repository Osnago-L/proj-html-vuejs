<template>
  <div class="social-section">
      <div class="jumbo-shop">
              <span class="title-header">try our season products</span>
              <h1 class="title">Order for pick-up or delivery to your home</h1>
              <button class="button-white">Shop Now</button>
      </div>
  </div>
</template>

<script>
export default {
    name: "ShopSection"
}
</script>

<style lang="scss" scoped>
.social-section{
    padding-top: 180px;


    .jumbo-shop{
    padding: 0 20%;
    height: 500px;
    background-image: url("../../assets/img/call-to-action-bg.jpg");
    background-size: cover;
    background-position: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
        h1{
            width: 60%;
            font-size: 40px;
            color: white;
            margin-top: 20px;
            margin-bottom: 80px;
        }
    }
}
</style>