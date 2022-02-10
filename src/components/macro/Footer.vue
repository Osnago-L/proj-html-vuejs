<template>
  <div class="footer container-footer">
    <div class="logo-map">
      <img src="../../assets/img/avada-bakery-logo-retina.png" alt="">
      <NavListItems/>
    </div>
    <div class="input-social">
      <div class="input">
        <h1 class="title">Subscribe to our Newsletter</h1>
        <div>
          <input placeholder="Enter Email Address..." type="text">
          <button class="button-purple">Subscribe</button>
        </div>
      </div>
      <div class="social">
        <i class="fa-brands fa-instagram"></i>
        <i class="fa-brands fa-twitter"></i>
        <i class="fa-brands fa-facebook-f"></i>
        <i class="fa-brands fa-pinterest-p"></i>
      </div>
    </div>
  </div>
</template>

<script>
import NavListItems from "../commons/NavListItems.vue";
export default {
    name: "Footer",
    components:{
      NavListItems
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/partial/variables.scss";
.footer{
  padding: 80px 0;
  height: 500px;
  display: flex;
  justify-content: space-between;
    
    .logo-map{
      display: flex;
      flex-direction: column;

      img{
        width: 180px;
        margin-bottom: 70px;
      }
    }

    .input-social{
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: flex-end;

      .input{
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        h1.title{
          font-size: 23px;
        }
        input{
          border: 1px solid rgba(0, 0, 0, 0.315);
          border-radius: 6px 6px;
          margin-right: 15px;
          padding: 0 10px;
          width: 400px;
          height: 37px;
          font-family: 'Roboto', sans-serif;
        }
      }
    }
    .social{
      display: flex;
      gap: 30px;
      svg{
        font-size: 18px;
        color: $daisy-bush;
        cursor: pointer;
      }
    }
}
</style>