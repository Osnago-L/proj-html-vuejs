<template>
  <div class="fixed-cart">
      <div class="cart">
          <i class="fa-solid fa-cart-shopping"></i>
          <span class="title-header">2</span>
      </div>
      <div class="total-cost">
          <span>27$</span>
      </div>
  </div>
</template>

<script>
export default {
    name:"FixedCart"

}
</script>

<style lang="scss" scoped>
.fixed-cart{
    position: fixed;
    top: 120px;
    right: 10px;
    z-index: 999;

    &>div{
        background-color: #e9dedc31;
        box-shadow: 1px 1px 8px rgba(0, 0, 0, 0.4);
        width: 60px;
        height: 60px;
        border-radius: 8px 8px;
        margin-bottom: 15px ;
    }
    .cart{
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
             cursor: pointer;

            svg{
                font-size: 35px;
            }
            span{
                position: absolute;
                top: 12.5px;
                right: 25px;
                margin-top: 3px;
                color:white;
                font-weight: 700;
            }
        }

    .total-cost{
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;

            span{
                font-size: 20px;
                color:#65bc7b;
                font-family: 'Roboto', sans-serif;
                font-weight: 700;
            }
    }
}
</style>