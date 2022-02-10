<template>
  <div class="header">
    <Nav/>
    <div class=" jumbo container">
      <div class="jumbo-text">
        <span class="title-header">Fresh & Tasty Bakery Every Day</span>
        <h1 class="title">The Perfect Fresh Bread</h1>
        <p class="subtitle-p">Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis nemo similique soluta officiis.</p>
        <button class="button-white">Explore our products</button>
      </div>
    </div>
  </div>
</template>

<script>
import Nav from "../sections/Nav.vue";

export default {
    name: "Header",
    components:{
      Nav
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/partial/variables.scss";

.header{
  width: 100%;
  height: 700px;
  max-height: 700px;
  background-image: url("../../assets/img/hero-header-bakery.jpg");
  background-color: #f5e9f3 ;
  background-repeat: no-repeat;
  background-position: bottom ;
  background-position-x: 200px;
  background-size: cover;
}
.jumbo{
  height: 100%;
  position: relative;
  top: 20%;

  .jumbo-text{
  width: 500px;

    & .title{
    // global overwrite
    font-size: 50px;
  }
  }
}

</style>
