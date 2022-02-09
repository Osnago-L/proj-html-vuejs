<template>
  <div class="social-section container">
      <div><img src="../../assets/img/social-1.jpg" alt=""></div>
      <div class="social-card grid-span-2">
          <span class="title-header">made for sharing</span>
          <h1 class="title">Let's stay in touch</h1>
          <button class="button-purple"><i class="fa-brands fa-instagram"></i> Follow Us</button>
      </div>
      <div><img src="../../assets/img/social-2.jpg" alt=""></div>
      <div><img src="../../assets/img/social-3.jpg" alt=""></div>
      <div><img src="../../assets/img/social-4.jpg" alt=""></div>
      <div><img src="../../assets/img/social-5.jpg" alt=""></div>
      <div><img src="../../assets/img/social-6.jpg" alt=""></div>

  </div>
</template>

<script>
export default {
    name: "SocialSection"
}
</script>

<style lang="scss" scoped>
.social-section{
    padding-top: 180px;

    display: grid;
    grid-template-columns: repeat(4,1fr);
    grid-template-rows: repeat(2,1fr);
    gap: 40px;

    .social-card{
        background-color: #e9dedc85;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    img{
        width: 100%;
        height: 100%;
        max-width: 100%;
        object-fit: cover;
        object-position: center;
    }

}
</style>