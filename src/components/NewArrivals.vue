<template>
  <div>
      <div class="ms-title d-flex">
        <span class="align-self-center"></span>
        <h2>New Arrivals</h2>
        <span class="align-self-center"></span>
      </div>
      <span>Brand new products from top designers</span>

      <ul class="d-flex ms-arrivals">
          <li><span><i class="fas fa-angle-left"></i></span></li>
          <li>
            <ul class="d-flex row row-cols-5">
                <li v-for="(item, index) in products" :key="index" :class="{ms_none : item.new_arrivals === false}">
                    <ul class="ms-card d-flex" v-if="item.new_arrivals === true">
                        <li><img :src="require(`../assets/img/${item.img_big}`)" alt=""></li>
                    </ul>
                </li>
            </ul>
          </li>
          <li><span><i class="fas fa-angle-right"></i></span></li>
      </ul>

  </div>
</template>

<script>

export default {
  name: 'NewArrivals',
  props: {
    products: Array,
  }
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

div {
    text-align: center;
    margin-top: 8rem;

    .ms-title {
        h2 {
            width: 40%;
        }
        span {
            height: 2px;
            background-color: #f1f1f1;
            width: calc((100% - 40%)/2 );
            margin: 0 2rem;
        }
    }

    .ms-arrivals {

        padding: 2rem 0;

        li {
            cursor: pointer;
            margin: auto;

            span {
                color: white;
                background-color: #c1c1c1;
                padding: 1rem .3rem;
            }

            .ms_none {
              display: none;
            }
        }
        img {
            width: 100%;
        }
    }
}

</style>