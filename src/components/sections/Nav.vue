<template>
  <div class="nav-header container">
    <img class="logo" src="../../assets/img/avada-bakery-logo-retina-200x97.png" alt="">
    <NavListItems/>
  </div>
</template>

<script>
import NavListItems from "../commons/NavListItems.vue";
export default {
  name: "Nav",
  components:{
    NavListItems
  }

}
</script>

<style lang="scss" scoped>
.nav-header{
  height: 100px;

  display: flex;
  align-items: center;
  justify-content: space-between;

  .logo{
  width: 150px;
  }
}
</style>