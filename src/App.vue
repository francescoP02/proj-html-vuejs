<template>
  <div id="app">
    <header>
      <AppHeader :iconSocial="iconSocial" />
    </header>

    <main>
      <AppJumbo />
      <FeaturedProducts :products="products" />
      <AppCollection />
      <BestSeller :products="products" />
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
      <AppFooterBottom />
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
import AppFooterBottom from './components/AppFooterBottom.vue'



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
    AppFooterBottom,
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
                img_big: "black_leather_jacket.jpg",
                featured: true,
                sale: false,
                top: false,
                reviews: false,
                featured_men: false,
                best_seller: true,
            },
            {
                name: "Black Leather Jacket",
                original_price: "$235",
                price: "$200",
                img: "black_elegant_leather_jacket-120x156.jpg",
                img_big: "black_elegant_leather_jacket.jpg",
                featured: true,
                sale: true,
                top: true,
                reviews: true,
                review: 5,
                user_review: "by admin",
                featured_men: true,
                best_seller: true,
            },
            {
                name: "Hipster Black Top",
                price: "$57",
                img: "hipster_black_top-120x156.jpg",
                img_big: "hipster_black_top.jpg",
                featured: true,
                sale: false,
                top: false,
                reviews: false,
                featured_men: false,
                best_seller: true,
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
                featured_men: false,
                best_seller: false,
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
                featured_men: false,
                best_seller: false,
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
                featured_men: false,
                best_seller: false,
            },
            {
                name: "Spring Printed Dress",
                original_price: "",
                price: "$47",
                img: "spring_printed_dress-120x156.jpg",
                img_big: "spring_printed_dress.jpg",
                featured: false,
                sale: false,
                top: true,
                reviews: true,
                review: 5,
                user_review: "by admin",
                featured_men: false,
                best_seller: true,
            },
            {
                img_big: "black_leather_suit.jpg",
                name: "Black Leather Suit",
                genre: "Men, Jackets",
                original_price: "",
                price: "$176",
                featured_men: true,
                best_seller: false,
            },
            {
                img_big: "blue_jacket_and_white_stripe_tee.jpg",
                name: "Blue Jacket & Stripe Tee",
                genre: "Men, Jackets, Suits",
                original_price: "",
                price: "$580",
                featured_men: true,
                best_seller: false
            },
            {
                img_big: "modern_black_leather_suit.jpg",
                name: "Modern Black Leather Suit",
                genre: "Men, Jackets",
                original_price: "",
                price: "$96",
                featured_men: true,
                best_seller: false
            },
            {
              img_big: "modern_love_tee.jpg",
              best_seller: true,
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
