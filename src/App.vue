<template>
  <div id="app">
    <header>
      <AppHeader />
    </header>

    <main>
      <AppMain />
    </main>

    <footer>
      <AppFooter />
    </footer>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'


export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter,
}
}
</script>

<style lang="scss">
@import "./style/common.scss";
@import "./style/variables.scss";

</style>
