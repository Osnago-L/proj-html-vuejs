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
  name: "FixedCart",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partial/variables.scss";
.fixed-cart {
  position: fixed;
  top: 120px;
  right: 10px;
  z-index: 999;

  & > div {
    background-color: rgba(white, 0.9);
    box-shadow: 1px 1px 8px rgba(black, 0.4);
    width: 60px;
    height: 60px;
    border-radius: 8px 8px;
    margin-bottom: 15px;
  }
  .cart {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;

    svg {
      font-size: 35px;
      color: $daisy-bush;
    }
    span {
      position: absolute;
      top: 12.5px;
      right: 25px;
      margin-top: 3px;
      color: white;
      font-weight: 700;
    }
  }

  .total-cost {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: rgba($daisy-bush, 0.9);
    cursor: pointer;

    span {
      font-size: 20px;
      color:white;
      font-family: $roboto;
      font-weight: 700;
    }
  }
}
</style>