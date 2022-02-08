<template>
  <div class="header">
    <Nav/>
    <div class=" jumbo container">
      <div class="jumbo-text">
        <span>Fresh & Tasty Bakery Every Day</span>
        <h1>The Perfect Fresh Bread</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis nemo similique soluta officiis.</p>
        <button>Explore our products</button>
      </div>
    </div>
  </div>
</template>

<script>
import Nav from "../commons/Nav.vue";

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

  &>span{
    font-size: 14px;
    text-transform: uppercase;
    color: #929295;
    font-family: 'Roboto', sans-serif;
  }
  &>h1{
    font-size: 50px;
    color: $daisy-bush;
    margin: 20px 0;
    font-family: 'Merriweather', serif;

  }
  &>p{
    font-size: 17px;
    color: #878589;
    margin-bottom: 30px;
    font-family: 'Roboto', sans-serif;
  }
  &>button{
    border: none;
    border-radius: 6px 6px;
    background-color: white;
    padding: 10px 30px;
    font-size: 14px;
    font-family: 'Roboto', sans-serif;
    color: $daisy-bush;
    cursor: pointer;
  }
  }
}

</style>
