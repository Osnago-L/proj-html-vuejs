<template>
  <div class="locations container">
      <span class="title-header">Locations</span>
      <h1 class="title">Visit our Bakeries</h1>
    <div>
        <div class="newyork">
            <img src="../../assets/img/new-york-bk.jpg" alt="">
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
            <img src="../../assets/img/london-bk.jpg" alt="">
            <div class="location-info">
                <h1 class="title">London</h1>
                <div>

                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: "Locations"
}
</script>

<style lang="scss" scoped>
.locations{
    padding-top: 140px;
    height: 800px;
    text-align: center;

    &>div{
        display: flex;
    }
    .newyork{
        background-color: #0a5d6c1c;
    }
    .london{
        background-color: #f0caa127;
    }

    .newyork,.london{
        width: 50%;
        height: 700px;

        img{
            width: 100%;
            height: 80%;
            object-fit: cover;
        }
    }
    .location-info{
        &>div{
            display: flex;
            justify-content: space-evenly;

            &>div{
                display: flex;
                flex-direction: column;
                justify-content: space-evenly;
            }
        }
    }
}
</style>