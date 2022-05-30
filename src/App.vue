<template>
  <div id="app">
    <header>
      <AppHeader />
    </header>

    <main>
      <AppJumbo />
      <FeaturedProducts />
      <AppMain />
    </main>

    <footer>
      <AppFooter />
    </footer>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppJumbo from './components/AppJumbo.vue'
import FeaturedProducts from './components/FeaturedProducts.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'




export default {
  name: 'App',
  components: {
    AppHeader,
    AppJumbo,
    FeaturedProducts,
    AppMain,
    AppFooter,
}
}
</script>

<style lang="scss">
@import "./style/common.scss";
@import "./style/variables.scss";

</style>
