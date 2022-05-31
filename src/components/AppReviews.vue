<template>
  <div class="ms-container">
      <div class="ms-review" v-for="(item,index) in review" :key="index" :class="{active : index === currentItem}">

      <img :src="require(`../assets/img/${item.img}`)" alt="">
      <span>{{item.review}}</span>
      <span>{{item.name}}, Theme Fusion</span>
      </div>

      <div class="form-check form-check-inline">
        <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio1" value="0" checked="checked" @click="clickedItem(0)">
        <label class="form-check-label" for="inlineRadio1">1</label>
      </div>
      <div class="form-check form-check-inline">
        <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio2" value="1" @click="clickedItem(1)">
        <label class="form-check-label" for="inlineRadio2">2</label>
      </div>

  </div>
</template>

<script>

export default {
  name: 'AppReviews',
  data: function() {
      return {
          currentItem: 0,
          review: [
              {
                  img: "man_testimonial.png",
                  review: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque semper orci tortor, in sagittis diam rhoncus sed. Proin justo est, convallis nec eleifend consectetur, blandit id dui.",
                  name: "Dario Pineda",
              },
              {
                  img: "woman_testimonial.png",
                  review: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque semper orci tortor, in sagittis diam rhoncus sed. Proin justo est, convallis nec eleifend consectetur, blandit id dui.",
                  name: "Anna Pineda",
              },
          ]
      }
  },
  methods: {
    clickedItem : function(number) {
        this.currentItem = number;
  },
  }
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";

.ms-container {
  background-image: url(../assets/img/testimonials_home_1_bg.jpg);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  color: #ffffff;
  text-align: center;
  padding: 2rem 0;
  margin-top: 4rem;

  .ms-review {
    display: none;
    width: 80%;
    margin: 0 auto;
    padding-bottom: 2rem;

    span {
      display: block;
    }
  }

  .active {
      display: block;
  }
}

</style>