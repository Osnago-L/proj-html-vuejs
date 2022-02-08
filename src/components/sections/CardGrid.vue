<template>
  <div class="card-grid container">
      <div class="card card01 grid-span-2">
          <div class="text-card">
                <h1 class="title-card">Tell us what you have in mind</h1>
                <span class="id-card">01</span>
            <div class="text-section">
                <span class="title-header-card">Manual Ingridient selection</span>
                <p class="subtitle-card">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aliquam, velit vero, labore temporibus eum porro, doloribus maxime dolor consequuntur odit necessitatibus architecto eaque ad facere aperiam dicta repellendus consectetur perferendis?</p>
            </div>
          </div>
      </div>
      <div class="card card02">
          <div class="text-card">
                <h1 class="title-card">We Start Baking</h1>
                <span class="id-card">02</span>
            <div class="text-section">
                <span class="title-header-card">Manual Ingridient selection</span>
                <p class="subtitle-card">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aliquam, velit vero, labore temporibus eum porro, doloribus maxime dolor consequuntur odit necessitatibus architecto eaque ad facere aperiam dicta repellendus consectetur perferendis?</p>
            </div>
          </div>
      </div>
      <div class="card quote">
          <span class="title-header">Don't just take out word for it</span>
          <h1 class="title">"Finally found an alternative to the mass produced products. Something that incorporates real organic ingredients, nutrient dense wellness while promoting sustainability and activity."</h1>
          <span class="author">Rachel Cooper, Founder</span>
      </div>
      <div class="card card03 grid-span-2">
          <div class="text-card">
                <h1 class="title-card">Delivered to your home</h1>
                <span class="id-card">03</span>
            <div class="text-section">
                <span class="title-header-card">Manual Ingridient selection</span>
                <p class="subtitle-card">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aliquam, velit vero, labore temporibus eum porro, doloribus maxime dolor consequuntur odit necessitatibus architecto eaque ad facere aperiam dicta repellendus consectetur perferendis?</p>
            </div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: "CardGrid"
}
</script>

<style lang="scss" scoped>
.test{
    justify-self: end;
}
.card-grid{
    padding-top: 140px;
    display: grid;
    gap: 25px;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3,1fr);

    .card{
        height: 700px;
        background-position: center;
        background-size: cover;

        &>.text-card{
            padding: 60px;
            height: 100%;
            width: 100%;
            background-color: rgba(0, 0, 0, 0.37);

            display: grid;
            grid-template-columns: repeat(2,1fr);

            &>*{
                color: rgba(255, 255, 255, 0.9);
            }

            & .title-card{
            font-size: 55px;
            font-family: 'Merriweather', serif;
            grid-area: h1;
            }
            & .id-card{
                font-size: 80px;
                font-family: 'Roboto', sans-serif;
                font-weight: 100;
                justify-self: end;
                grid-area: span;
            }
            & .title-header-card{
                font-size: 13px;
                font-family: 'Roboto', sans-serif;
                color: #c5c5c7;
                text-transform: uppercase;
            }
            & .subtitle-card{
                margin-top: 15px;
                font-size: 18px;
                font-family: 'Roboto', sans-serif;
                line-height: 28px;
            }
            .text-section{
            grid-area: div;
        }
        }
    }
    .card01{
        background-image: url("../../assets/img/bakery-process-1.jpg");

        & .text-card{
            grid-template-areas: "h1 span" ". div" ;
        }
        & .text-section{
            justify-self: end;
            align-self: center;
            width: 550px;
        }

    }
    .card02{
        background-image: url("../../assets/img/bakery-process-2.jpg");
        & .text-card{
            grid-template-areas: "h1 span" "div ." ;
        }
        & .text-section{
            align-self: end;
            width: 450px;
        }
    }
    .card03{
        background-image: url("../../assets/img/bakery-process-3.jpg"); 
        & .text-card{
            grid-template-areas: "h1 span" "div ." ;
        }
        & .text-section{
            align-self: end;
            width: 550px;
        }
    }
    .quote{
        padding: 90px 80px;
        background-color: #e9dedc;
        overflow-y: auto;

        & .title{
            font-size: 45px;
            margin: 40px 0;
        }

        & .author{
            font-size: 13px;
            color: #878589;
            font-family: 'Roboto', sans-serif;
        }
    }
}

</style>