<template>
  <div class="locations container">
    <span class="title-header">Locations</span>
    <h1 class="title">Visit our Bakeries</h1>
    <div>
      <div class="newyork">
        <img src="../../assets/img/new-york-bk.jpg" alt="" />
        <div class="location-info">
          <h1 class="title">New York</h1>
          <div>
            <div>
              <span class="title-header">Call Us</span>
              <span class="subtitle-p">1.800.455.556</span>
            </div>
            <div>
              <span class="title-header">Open All Week</span>
              <span class="subtitle-p">9.00 AM - 6.00PM</span>
            </div>
            <button class="button-white">View Map</button>
          </div>
        </div>
      </div>
      <div class="london">
        <img src="../../assets/img/london-bk.jpg" alt="" />
        <div class="location-info">
          <h1 class="title">London</h1>
          <div>
            <div>
              <span class="title-header">Call Us</span>
              <span class="subtitle-p">1.800.455.556</span>
            </div>
            <div>
              <span class="title-header">Open All Week</span>
              <span class="subtitle-p">9.00 AM - 6.00PM</span>
            </div>
            <button class="button-white">View Map</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Locations",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partial/variables.scss";
.locations {
  padding-top: 140px;
  text-align: center;

  & > div {
    display: flex;
  }
  .newyork {
    background-color: rgba($atoll, 0.1);
  }
  .london {
    background-color: rgba($chalky, 0.1);
  }

  .newyork,
  .london {
    width: 50%;
    height: 700px;

    img {
      width: 100%;
      height: 80%;
      object-fit: cover;
    }
  }
  .location-info {
    & > div {
      display: flex;
      align-items: flex-start;
      justify-content: space-evenly;

      & > div {
        width: 120px;
        display: flex;
        flex-direction: column;

        & span:first-child {
          font-size: 13px;
        }
        & span:nth-child(2) {
          font-size: 13px;
        }
      }
    }
  }
}
</style>