<template>
  <div class="main">
    <Products/>
    <Weddings/>
    <ProductsPrices/>
    <CardGrid/>
    <Locations/>
  </div>
</template>

<script>
import Products from "../sections/Products.vue";
import Weddings from "../sections/Weddings.vue";
import ProductsPrices from "../sections/ProductsPrices.vue";
import CardGrid from "../sections/CardGrid.vue";
import Locations from "../sections/Locations.vue";

export default {
    name: "Main",
    components:{
      Products,
      Weddings,
      ProductsPrices,
      CardGrid,
      Locations
    }
}
</script>

<style lang="scss" scoped>

</style>
