<template>
  <div class="header">
    <Nav/>
    <div class=" jumbo container">
      <div class="jumbo-text">
        <span>Fresh & Tasty Bakery Every Day</span>
        <h1 class="title">The Perfect Fresh Bread</h1>
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
  background-repeat: repeat;
  background-position: bottom ;
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
    color: #929295;
  }
  &>.title{
    font-size: 50px;
    color: $daisy-bush;
    margin: 10px 0;
  }
  &>p{
    font-size: 17px;
    color: #929295;
    margin-bottom: 20px;
  }
  &>button{
    border: none;
    border-radius: 6px 6px;
    background-color: white;
    padding: 10px 30px;
    font-size: 14px;
    color: $daisy-bush;
    cursor: pointer;
  }
  }
}

</style>
