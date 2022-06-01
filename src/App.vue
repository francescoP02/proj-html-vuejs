<template>
  <div id="app">
    <header>
      <AppHeader :iconSocial="iconSocial" />
    </header>

    <main>
      <AppJumbo />
      <FeaturedProducts />
      <AppCollection />
      <BestSeller />
      <AppPromo />
      <NewArrivals />
      <AppReviews />
      <AppBlog />
      <AppProduct :products="products" />
      <AppBrand />
    </main>

    <footer>
      <AppSubscribe />
      <AppFooter :iconSocial="iconSocial" :products="products" />
    </footer>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppJumbo from './components/AppJumbo.vue'
import FeaturedProducts from './components/FeaturedProducts.vue'
import AppCollection from './components/AppCollection.vue'
import BestSeller from './components/BestSeller.vue'
import AppPromo from './components/AppPromo.vue'
import NewArrivals from './components/NewArrivals.vue'
import AppReviews from './components/AppReviews.vue'
import AppBlog from './components/AppBlog.vue'
import AppProduct from './components/AppProduct.vue'
import AppBrand from './components/AppBrand.vue'
import AppSubscribe from './components/AppSubscribe.vue'
import AppFooter from './components/AppFooter.vue'



export default {
  name: 'App',
  components: {
    AppHeader,
    AppJumbo,
    FeaturedProducts,
    AppCollection,
    BestSeller,
    AppPromo,
    NewArrivals,
    AppReviews,
    AppBlog,
    AppProduct,
    AppBrand,
    AppSubscribe,
    AppFooter,
  },
  data: function() {
    return {
        iconSocial: [
        {
          name: "Facebook",
          icon: "fa-facebook-f",
        },
        {
          name: "Twitter",
          icon: "fa-twitter",
        },
        {
          name: "Instragram",
          icon: "fa-instagram",
        },
        {
          name: "Youtube",
          icon: "fa-youtube",
        },
      ],
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

<style lang="scss">
@import "./style/common.scss";
@import "./style/variables.scss";

</style>
