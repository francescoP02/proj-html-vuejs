<template>
  <div class="ms-product">
      <div class="container">

          <ul class="row row-cols-4">
              <li>
                  <ul class="ms-list-products">
                      <li><h5>FEATURED</h5></li>
                      <li class="ms-card" v-for="(item,index) in products" :key="index">
                        <ul v-if="item.featured === true" class="d-flex ms-row">
                            <li class="ms-text">
                                <div>
                                    <span class="ms-name">{{item.name}}</span>
                                    <span class="ms-review" v-if="item.reviews === true"><i v-for="n in 5" :key="n" class="fa-star" :class="n <= item.review ? 'fas' : 'far'"></i></span>
                                    <span class="ms-original" v-if="item.sale === true"> {{item.original_price}}</span>
                                    <span class="ms-price">{{item.price}}</span>
                                </div>
                            </li>
                            <li class="d-flex ms-img"><img :src="require(`../assets/img/${item.img}`)" alt=""></li>
                        </ul>
                      </li>
                  </ul>
              </li>
              <li>
                  <ul class="ms-list-products">
                      <li><h5>ON SALE</h5></li>
                      <li class="ms-card" v-for="(item,index) in products" :key="index">
                        <ul v-if="item.sale === true" class="d-flex ms-row">
                            <li class="ms-text">
                                <div>
                                    <span class="ms-name">{{item.name}}</span>
                                    <span class="ms-review" v-if="item.reviews === true"><i v-for="n in 5" :key="n" class="fa-star" :class="n <= item.review ? 'fas' : 'far'"></i></span>
                                    <span class="ms-original" v-if="item.sale === true"> {{item.original_price}}</span>
                                    <span class="ms-price">{{item.price}}</span>
                                </div>
                            </li>
                            <li class="d-flex ms-img"><img :src="require(`../assets/img/${item.img}`)" alt=""></li>
                        </ul>
                      </li>
                  </ul>
              </li>
              <li>
                  <ul class="ms-list-products">
                      <li><h5>TOP RATED</h5></li>
                      <li class="ms-card" v-for="(item,index) in products" :key="index">
                        <ul v-if="item.top === true" class="d-flex ms-row">
                            <li class="ms-text">
                                <div>
                                    <span class="ms-name">{{item.name}}</span>
                                    <span class="ms-review" v-if="item.reviews === true"><i v-for="n in 5" :key="n" class="fa-star" :class="n <= item.review ? 'fas' : 'far'"></i></span>
                                    <span class="ms-original" v-if="item.sale === true"> {{item.original_price}}</span>
                                    <span class="ms-price">{{item.price}}</span>
                                </div>
                            </li>
                            <li class="d-flex ms-img"><img :src="require(`../assets/img/${item.img}`)" alt=""></li>
                        </ul>
                      </li>
                  </ul>
              </li>
              <li>
                  <ul class="ms-list-products">
                      <li><h5>LATEST REVIEWS</h5></li>
                      <li class="ms-card" v-for="(item,index) in products" :key="index">
                        <ul v-if="item.reviews === true" class="d-flex ms-row">
                            <li class="ms-text">
                                <div>
                                    <span class="ms-name">{{item.name}}</span>
                                    <span class="ms-review" v-if="item.reviews === true"><i v-for="n in 5" :key="n" class="fa-star" :class="n <= item.review ? 'fas' : 'far'"></i></span>
                                    <span>{{item.user_review}}</span>
                                </div>
                            </li>
                            <li class="d-flex ms-img"><img :src="require(`../assets/img/${item.img}`)" alt=""></li>
                        </ul>
                      </li>
                  </ul>
              </li>
          </ul>

      </div>
      
  </div>
</template>

<script>

export default {
  name: 'AppProduct',
  data: function() {
      return {
          products: [
              {
                  name: "Black Jacket",
                  price: "$125",
                  img: "black_leather_jacket-120x156.jpg",
                  featured: true,
                  sale: false,
                  top: false,
                  reviews: false,
              },
              {
                  name: "Black Leather Jacket",
                  original_price: "$235",
                  price: "$200",
                  img: "black_elegant_leather_jacket-120x156.jpg",
                  featured: true,
                  sale: true,
                  top: true,
                  reviews: true,
                  review: 5,
                  user_review: "by admin",
              },
              {
                  name: "Hipster Black Top",
                  price: "$57",
                  img: "hipster_black_top-120x156.jpg",
                  featured: true,
                  sale: false,
                  top: false,
                  reviews: false,
              },
              {
                  name: "Blue Leather Jacket",
                  original_price: "$80",
                  price: "$60",
                  img: "blue_leather_jacket-120x156.jpg",
                  featured: false,
                  sale: true,
                  top: false,
                  reviews: false,
              },
              {
                  name: "Modern Leather Boots",
                  original_price: "$50",
                  price: "$30",
                  img: "modern_leather_boots-120x156.jpg",
                  featured: false,
                  sale: true,
                  top: false,
                  reviews: false,
              },
              {
                  name: "Leather Gloves",
                  original_price: "",
                  price: "$45",
                  img: "leather_gloves-120x156.jpg",
                  featured: false,
                  sale: false,
                  top: true,
                  reviews: true,
                  review: 5,
                  user_review: "by Beardman",
              },
              {
                  name: "Spring Printed Dress",
                  original_price: "",
                  price: "$47",
                  img: "spring_printed_dress-120x156.jpg",
                  featured: false,
                  sale: false,
                  top: true,
                  reviews: true,
                  review: 5,
                  user_review: "by admin",
              },
          ]
      }
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

.ms-product {
    border-top: 2px solid #f1f1f1;
    padding-top: 4rem;

    .ms-list-products {

        
        .ms-card {
            display: block;

            .ms-row {
                border-bottom: 1px solid #f1f1f1;
                padding-left: 0;
                padding: 1rem 0;
                cursor: pointer;

                .ms-text {
                    width: 70%;
                    flex-direction: row;
                    color: #8d858a;
                    padding-left: 0;

                    .ms-name {
                        margin-right: .3rem;
                    }
                    .ms-review {
                        display: block;
                        color: #427ed1;
                        padding: .5rem 0;
                    }
                    .ms-original {
                        text-decoration: line-through;
                        color: #4a5660;
                        font-weight: 700;
                    }
                    .ms-price {
                        color: #4a5660;
                        font-weight: 500;
                    }
                }

                .ms-img {
                    width: 30%;
                    img {
                        width: 100%;
                        padding: .5rem;
                    }
                }
            }
        }
    }
}

</style>