<template>
  <div id="app">
    <header>
      <AppHeader />
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
      <AppProduct />
      <AppBrand />
    </main>

    <footer>
      <AppSubscribe />
      <AppFooter />
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
}
}
</script>

<style lang="scss">
@import "./style/common.scss";
@import "./style/variables.scss";

</style>
