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

      <ul class="d-flex row row-cols-4">
        <li class="ms-featured" v-for="(item, index) in featuredCard" :key="index">
            <ul class="ms-card">
                <li><img :src="require(`../assets/img/${item.img}`)" alt=""></li>
                <li><h5>{{item.name}}</h5></li>
                <li><span class="ms-genre"> {{item.genre}} </span></li>
                <li><span class="ms-original-price" v-if="item.original_price !== ''  ">{{item.original_price}}</span> <span class="ms-price">{{item.price}}</span></li>
            </ul>
        </li>
      </ul>
  </div>
</template>

<script>

export default {
  name: 'FeaturedProducts',
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
        featuredCard: [
            {
                img: "black_elegant_leather_jacket.jpg",
                name: "Black Leather Jacket",
                genre: "Men, Jackets, Jeans",
                original_price: "$235",
                price: "$200",
            },
            {
                img: "black_leather_suit.jpg",
                name: "Black Leather Suit",
                genre: "Men, Jackets",
                original_price: "",
                price: "$176",
            },
            {
                img: "blue_jacket_and_white_stripe_tee.jpg",
                name: "Blue Jacket & Stripe Tee",
                genre: "Men, Jackets, Suits",
                original_price: "",
                price: "$580",
            },
            {
                img: "modern_black_leather_suit.jpg",
                name: "Modern Black Leather Suit",
                genre: "Men, Jackets",
                original_price: "",
                price: "$96",
            },
        ]
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
            border: 1px solid #f1f1f1
        }
        .active{
        background-color: white;
        }
    }

    .ms-card {
        li {
            display: block;
            margin-top: .3rem;
            text-align: left;

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

</style>