<template>
  <div class="ms-footerbottom">

    <div class="container">
      <span>© Copyright 2012 - 2020 | Avada Theme by Theme Fusion | All Rights Reserved | Powered by WordPress</span>
        <img src="../assets/img/payment_cards_footer.png" alt="">
    </div>
      
  </div>
</template>

<script>

export default {
  name: 'AppFooterBottom',

}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";

ul {
  list-style: none;
}

li {
  display: inline-block;
}

.ms-footerbottom {

    background-color: #1d1f22;
    padding: 1rem 0;

    .container {
    text-align: center;
        span {
            display: block;
            color: $footer-color;
            padding: 1rem 0;
            font-size: .8rem;
        }
    }

}


</style>