<template>
  <div class="ms-jumbo">
      <div class="ms-jumbotext">
          <h1>Brand New Arrivals</h1>
          <span>NEW COLLECTION FROM NEW YORK</span>
          <div>
            <button type="button" class="btn btn-outline-light rounded-pill">VIEW ALL</button>
            <button type="button" class="btn btn-outline-light rounded-pill">LOOKBOOK</button>
          </div>
      </div>  
  </div>
</template>

<script>

export default {
  name: 'AppJumbo',
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";

.ms-jumbo {
    height: 90vh;
    background-image: url(../assets/img/home1_slide_three_bg_2.jpg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: auto;
    position: relative;

    .ms-jumbotext {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
        color: #ffffff;
        h1 {
            font-size: 5.5rem;
        }

        span {
            display: block;
            font-size: 2rem;
            text-align: center;
            padding-bottom: 2rem;
        }

        div {

            text-align: center;

            button {
                font-size: 1rem;
                border: 3px solid white;
                padding: 1rem 2rem;
                margin-left: 1rem;
            }
        }

    }
}

</style>