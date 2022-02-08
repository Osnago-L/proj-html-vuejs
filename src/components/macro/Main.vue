<template>
  <div class="main">
    <Products/>
    <Weddings/>
    <ProductsPrices/>
    <CardGrid/>
  </div>
</template>

<script>
import Products from "../sections/Products.vue";
import Weddings from "../sections/Weddings.vue";
import ProductsPrices from "../sections/ProductsPrices.vue";
import CardGrid from "../sections/CardGrid.vue";

export default {
    name: "Main",
    components:{
      Products,
      Weddings,
      ProductsPrices,
      CardGrid
    }
}
</script>

<style lang="scss" scoped>

</style>
