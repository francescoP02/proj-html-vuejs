<template>
  <div class="ms-footer">
      <div class="container">
        <ul class="row row-cols-4 d-flex ms-col">
          <li class="ms-contacts">
            <ul class="d-flex">
              <li class="ms-footer-logo"><img src="../assets/img/classic_shop_logo_footer.png" alt=""></li>
              <li>12345 North Main Street,</li>
              <li>New York, NY 555555</li>
              <li>Phone: 1.800.555.6789</li>
              <li>Email: info@company.com</li>
              <li>Web: Theme-fusion.com</li>
              <li>
                <ul class="ms-social d-flex">
                  <li class="align-items-center px-1" v-for="(item, index) in iconSocial" :key="index"><i class="fab" :class="item.icon"></i></li>
                </ul>
              </li>
            </ul>
          </li>
          <li class="ms-top-rated">
            <ul>
              <li class="ms-title">TOP RATED PRODUCTS</li>
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
          <li class="ms-posts">
            <ul>
              <li class="ms-title">RECENT POSTS</li>
              <li class="ms-post" v-for="(item,index) in posts" :key="index"><span><i class="fas fa-angle-right"></i></span>{{item.post}}</li>
            </ul>
          </li>
          <li class="ms-tags">
            <ul>
              <li class="ms-title d-block">TAGS</li>
              <li>
                <ul class="d-flex flex-wrap ms-tag-group">
                  <li class="ms-tag" v-for="(item,index) in tags" :key="index">{{item.name}}</li>
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
  name: 'AppFooter',
  props: {
    iconSocial: Array,
    products: Array,
  },
  data: function() {
    return {
      posts: [
        {
          post: "Aenean lobortis sapien enim viverra",
        },
        {
          post: "Duis ac massa semper maximus",
        },
        {
          post: "Nunc fermint nulla eu justo sem id",
        },
        {
          post: "Aliquam posuere magna eget nibh",
        },
        {
          post: "Cras ac nulla ac consecte rutrum",
        },
        {
          post: "Fusce mattis nunc ut aliquam",
        },
      ],
      tags: [
        {
          name: "Black",
        },
        {
          name: "boots",
        },
        {
          name: "Brown",
        },
        {
          name: "Casual",
        },
        {
          name: "D&G",
        },
        {
          name: "Fabric",
        },
        {
          name: "flowers",
        },
        {
          name: "Grey",
        },
        {
          name: "hat",
        },
        {
          name: "Hipster",
        },
        {
          name: "lines",
        },
        {
          name: "multi-purpose",
        },
        {
          name: "New York",
        },
        {
          name: "Outdoors",
        },
        {
          name: "red",
        },
        {
          name: "responsive",
        },
        {
          name: "summer",
        },
        {
          name: "sweater",
        },
        {
          name: "Travel",
        },
        {
          name: "Warm",
        },
        {
          name: "White",
        },
        {
          name: "winter",
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

.ms-footer {
  background-color: #2b2e32;
  color: #ffffff;

  .ms-col {
    margin-bottom: 0;
    padding-top: 3rem;
    padding-bottom: 1rem;

    ul {
      padding-left: 0;
      .ms-title {
        padding-bottom: 2rem;
      }
    }

    .ms-contacts {
      ul {
        flex-direction: column;

        .ms-footer-logo {
          padding-bottom: 3rem;

          img {
            width: 50%;
          }

        }

        li {
          padding-top: .5rem;
          color: $footer-color;

          .ms-social {
            flex-direction: row;
            cursor: pointer;
          }
        }
      }
    }

    .ms-top-rated {
      color: $footer-color;

      .ms-card {
          display: block;

          .ms-row {
              border-bottom: 1px solid grey;
              padding-left: 0;
              padding: 1rem 0;
              cursor: pointer;

              .ms-text {
                  width: 70%;
                  flex-direction: row;
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
                      font-weight: 700;
                  }
                  .ms-price {
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

    .ms-posts {
      color: $footer-color;

      .ms-post {
        border-bottom: 1px solid $footer-color;
        padding: .8rem 0;
        cursor: pointer;
      }
      span {
        padding-right: .4rem;
      }
    }

    .ms-tags {
      color: $footer-color;
      .ms-tag {
        padding: .4rem;
        border: 1px solid $footer-color;
        cursor: pointer;
      }

      .ms-tag-group {
        gap: 10px;
      }
    }
  }
}

</style>