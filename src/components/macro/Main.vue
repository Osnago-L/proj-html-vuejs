<template>
  <div class="main">
    <Products/>
    <Weddings/>
    <ProductsPrices/>
    <CardGrid/>
    <Locations/>
    <SocialSection/>
    <ShopSection/>
  </div>
</template>

<script>
import Products from "../sections/Products.vue";
import Weddings from "../sections/Weddings.vue";
import ProductsPrices from "../sections/ProductsPrices.vue";
import CardGrid from "../sections/CardGrid.vue";
import Locations from "../sections/Locations.vue";
import SocialSection from "../sections/SocialSection.vue";
import ShopSection from "../sections/ShopSection.vue";

export default {
    name: "Main",
    components:{
      Products,
      Weddings,
      ProductsPrices,
      CardGrid,
      Locations,
      SocialSection,
      ShopSection
    }
}
</script>

<style lang="scss" scoped>

</style>
