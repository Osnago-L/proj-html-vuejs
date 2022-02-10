<template>
    <nav>
        <span v-for="element,index in items" :key="index"
        >{{element.name}}</span>

        <i class="fa-solid fa-cart-shopping"></i>
    </nav>
</template>

<script>
import {navItems} from "../../assets/javascript/data";
export default {
    name: "NavListItems",
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
nav{

    display: flex;
    gap: 50px;
   
    span{
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
    svg{
        font-size: 14px;
        color: $daisy-bush;

    &:hover{
        cursor: pointer;
    }
    }
    }
</style>