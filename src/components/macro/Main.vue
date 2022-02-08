<template>
  <div class="main">
    <Products/>
    <Weddings/>
    <ProductsPrices/>
  </div>
</template>

<script>
import Products from "../sections/Products.vue";
import Weddings from "../sections/Weddings.vue";
import ProductsPrices from "../sections/ProductsPrices.vue";

export default {
    name: "Main",
    components:{
      Products,
      Weddings,
      ProductsPrices
    }
}
</script>

<style lang="scss" scoped>

</style>
