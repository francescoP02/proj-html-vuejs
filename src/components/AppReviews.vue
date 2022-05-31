<template>
  <div>
      <div class="ms-review" v-for="(item,index) in review" :key="index" :class="{active : index === currentItem}">

      <img :src="require(`../assets/img/${item.img}`)" alt="">
      <span>{{item.review}}</span>
      <span>{{item.name}}, Theme Fusion</span>
      </div>
      <div class="form-check form-check-inline">
        <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio1" value="0" checked="checked" @click="clickedItem(val())">
        <label class="form-check-label" for="inlineRadio1">1</label>
      </div>
      <div class="form-check form-check-inline">
        <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio2" value="1" @click="clickedItem(val())">
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
          value: 0,
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
    clickedItem : function() {
        console.log(value);
  },
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";

.ms-review {
    display: none;

    .active {
        display: block;
    }
}

</style>