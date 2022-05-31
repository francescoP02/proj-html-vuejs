<template>
  <div class="ms-container">
      <div class="container row row-cols-2">
          <div class="ms-card" v-for="(item,index) in promoCard" :key="index">
            <img :src="require(`../assets/img/${item.img}`)" alt="">

            <div class="ms-text">
                <h2>{{item.name}}</h2>
                <span>{{item.description}}</span>
                <button type="button" class="btn btn-outline-light rounded-pill">VIEW MORE</button>
            </div>
          </div>
      </div>
      
  </div>
</template>

<script>

export default {
  name: 'AppPromo',
  data: function() {
      return {
          promoCard: [
              {
                  img: "promo_box_1_bg.jpg",
                  name: "70% Off",
                  description: "Vivamus tempor leo lacus, feugiat ut magna aliquat erat.",
              },
              {
                  img: "promo_box_2_bg.jpg",
                  name: "Free Shipping",
                  description: "Vivamus tempor leo lacus, feugiat ut magna aliquat erat.",
              },
          ]
      }
  },
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";


.ms-container {
    background-image: url(../assets/img/bkgd_confetti-compressor.jpg);
    background-position: center;
    background-size: cover;
    padding: 5rem 0;
    margin-top: 5rem;
}

.container {
    margin: 0 auto;

    img {
    width: 100%;
    position: relative;
    }   

    .ms-card {
        position: relative;

        .ms-text {
            position: absolute;
            top: 50%;
            left: 45%;
            transform: translate(-50%,-50%);
            color: #ffffff;

            h2 {
                font-weight: 700;
            }

            span {
                margin: 2rem 0;
            }

            button{
                display: block;
                margin: 1rem 0;
            }
        }
    }

}


</style>