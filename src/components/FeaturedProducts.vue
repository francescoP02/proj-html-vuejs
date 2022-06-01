<template>
  <div class="container">
      <div class="ms-title d-flex">
        <span class="align-self-center"></span>
        <h2>Featured Products</h2>
        <span class="align-self-center"></span>
      </div>
      <span>Must have products from our top sellers</span>
      <ul class="ms-featuredmenu my-4">
          <li v-for="(item, index) in featuredMenu" :key="index" @click="clickedItem(index)" :class="{active : index === currentItem}"> {{item.name}}</li>
      </ul>

      <ul class="ms-card row row-cols-4">
        <li class="ms-featured" v-for="(item, index) in products" :key="index" :class="{ms_none : item.featured_men === false}">
            <ul v-if="item.featured_men === true" class="ms-card">
                <li>
                    <div>
                        <img :src="require(`../assets/img/${item.img_big}`)" alt="">
                        <h5>{{item.name}}</h5>
                        <span class="ms-genre"> {{item.genre}} </span>
                        <span class="ms-original-price" v-if="item.original_price !== ''  ">{{item.original_price}}</span> <span class="ms-price">{{item.price}}</span>
                    </div>
                </li>
            </ul>
        </li>
      </ul>
  </div>
</template>

<script>

export default {
  name: 'FeaturedProducts',
  props: {
      products: Array,
  },
  data: function() {
    return {
        currentItem: 0,
        featuredMenu: [
            {
                name: "Men",
                active: false,
            },
            {
                name: "Woman",
                active: false,
            },
            {
                name: "Accessories",
                active: false,
            },
        ],
    };
  },

  methods: {
    clickedItem : function(index) {
        this.currentItem = index;
    },
  },
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

.container {
    text-align: center;
    margin-top: 8rem;
    margin-bottom: 8rem;

    .ms-title {
        h2 {
            width: 40%;
        }
        span {
            height: 2px;
            background-color: #f1f1f1;
            width: calc((100% - 40%)/2 )
        }
    }

    .ms-featuredmenu {
        padding: 1rem;
        li {
            background-color: #f1f1f1;
            padding: 1rem 3rem;
            border: 1px solid #f1f1f1;
            cursor: pointer;
        }
        .active{
        background-color: white;
        }
    }

    .ms_none {
        display: none;
    }

    .ms-card {
        li {

            div {
                text-align: left;

                h5 {
                    margin-top: .3rem;
                }

                img {
                    width: 100%;
                }

                .ms-genre {
                    color: #383e3f;
                }

                .ms-original-price {
                    color: #5a98d8;
                    text-decoration: line-through;
                }

                .ms-price {
                    color: #5a98d8;
                }

            }
        }
    }

}

</style>