<template>
  <div class="nav-header container">
    <img class="logo" src="../../assets/img/avada-bakery-logo-retina-200x97.png" alt="">
    <nav>
        <span v-for="element,index in items" :key="index"
        >{{element.name}}</span>

        <i class="fa-solid fa-cart-shopping"></i>
    </nav>
  </div>
</template>

<script>
import {navItems} from "../../assets/javascript/data";
export default {
  name: "Nav",
  data(){
    return{
      items:[]
    }
  },
  created(){
    this.items = navItems
  }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/partial/variables.scss";
.nav-header{
  height: 100px;

  display: flex;
  align-items: center;
  justify-content: space-between;

  .logo{
  width: 150px;
  }
  nav{
    i{
        font-size: 14px;
        margin: 0 30px;

      &:hover{
        cursor: pointer;
      }
    }
    
    span{
      margin: 0 30px;
      padding-bottom: 8px;
      text-transform: uppercase;
      font-weight: 700;
      font-size: 12px;
      font-family: 'Roboto', sans-serif;
      color: $daisy-bush;
      opacity: 0.8;

      &:hover{
        font-weight: 700;
        border-bottom: 2px solid $daisy-bush;
        cursor: pointer;
      }
    }
    }
}

</style>