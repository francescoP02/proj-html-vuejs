<template>
  <div  class="ms-logo">
      <div class="ms-container">
          <h5 class="ms-title col-12 text-center">BRAND LOGOS</h5>
          <div class="row row-cols-5">
            <span v-for="(item,index) in logos" :key="index">
                <img :src="require(`../assets/img/${item.img}`)" alt="">
            </span>
          </div>
      </div>
  </div>
</template>

<script>

export default {
  name: 'AppBrand',
  data: function() {
      return {
          logos: [
              {
                  img: "b_logotype_6.png",
              },
              {
                  img: "b_logotype_7.png",
              },
              {
                  img: "b_logotype_1.png",
              },
              {
                  img: "b_logotype_2.png",
              },
              {
                  img: "b_logotype_3.png",
              },
          ]
      }
  },
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";

.ms-logo {
    background-color: #f6f6f6;

    .ms-container {
        margin: 0 auto;
        width: 60%;

        .ms-title {
            padding-top: 2rem;
            font-weight: 400;
        }

        .row {
            padding: 3rem 0 3rem;

            img {
                cursor: pointer;
                width: 100%;
            }

        }
    }
}




</style>