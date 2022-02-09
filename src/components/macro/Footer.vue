<template>
  <div class="footer container-footer">
    <div class="logo-map">
      <img src="../../assets/img/avada-bakery-logo-retina.png" alt="">
      <div class="map">
        <span>Test</span>
        <span>Test</span>
        <span>Test</span>
        <span>Test</span>
        <span>Test</span>
        <span>Test</span>
        <span>Test</span>
        <span>Test</span>
      </div>
    </div>
    <div></div>
  </div>
</template>

<script>
export default {
    name: "Footer"
}
</script>

<style lang="scss" scoped>
.footer{
  padding: 80px 0;
    height: 500px;
    
    .logo-map{
      display: flex;
      flex-direction: column;

      img{
        width: 200px;
      }
      .map{
        margin-top: 80px;
        display: flex;
        gap: 70px;
      }
    }
}
</style>