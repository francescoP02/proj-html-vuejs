<template>
  <div>
      <div class="container">
        <ul class="row row-cols-4 d-flex">
          <li>
            <ul>
              <li><img src="../assets/img/classic_shop_logo1x.png" alt=""></li>
              <li>12345 North Main Street,</li>
              <li>New York, NY 555555</li>
              <li>Phone: 1.800.555.6789</li>
              <li>Email: info@company.com</li>
              <li>Web: Theme-fusion.com</li>
              <li>
                <ul class="ms-social d-flex">
                  <li class="align-items-center" v-for="(item, index) in iconSocial" :key="index"><i class="fab" :class="item.icon"></i></li>
                </ul>
              </li>
            </ul>
          </li>
          <li>
            <ul>
              <li>TOP RATED PRODUCTS</li>
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
            <ul>
              <li>RECENT POSTS</li>
              <li v-for="(item,index) in posts" :key="index">{{item.post}}</li>
            </ul>
          </li>
          <li>
            <ul>
              <li>TAGS</li>
              <li v-for="(item,index) in tags" :key="index">{{item.name}}</li>
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

</style>