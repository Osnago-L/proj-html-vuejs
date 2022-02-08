<template>
  <div class="main">
    <Products/>
    <Weddings/>
  </div>
</template>

<script>
import Products from "../sections/Products.vue";
import Weddings from "../sections/Weddings.vue";

export default {
    name: "Main",
    components:{
      Products,
      Weddings
    }
}
</script>

<style lang="scss" scoped>

</style>
