<template>
  <div class="weddings container">
      <span class="title-header">Corporate & Weddings</span>
      <h1 class="title">Baking Special Moment</h1>
      <div class="wedding-images">
            <div @mouseover="hoverImage" v-for="element,index in item" :key="index">
                <img :src="hoverImage()? element.imgHover : element.img"  alt="">
                <div>
                    
                </div>
            </div>

      </div>
  </div>
</template>

<script>
import { corporateWedding } from "../../assets/javascript/data";
export default {
    name: "Weddings",
    data(){
        return{
            items:"",
            hoveritem:""
        }
    },
    methods:{
        hoverImage(){
            return true;
        }
    },
    created(){
        this.item = corporateWedding
    }
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