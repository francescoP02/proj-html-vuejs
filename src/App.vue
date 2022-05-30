<template>
  <div id="app">
    <header>
      <AppHeader />
    </header>

    <main>
      <AppJumbo />
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
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'



export default {
  name: 'App',
  components: {
    AppHeader,
    AppJumbo,
    AppMain,
    AppFooter,
}
}
</script>

<style lang="scss">
@import "./style/common.scss";
@import "./style/variables.scss";

</style>
