<script>
import AppHeader from './components/AppHeader.vue';
import AppNav from './components/AppNav.vue';
import Appjumbo from './components/AppJumbo.vue';
import AppFooter from './components/AppFooter.vue';
import AppMain from './components/AppMain.vue'
export default {
  components: {
    AppHeader,
    AppNav,
    Appjumbo,
    AppFooter,
    AppMain
  }
}
</script>

<template lang="">
  <div>
    <AppHeader />
    <AppNav />
    <Appjumbo />
    <AppMain />
    <AppFooter />
  </div>
</template>

<style lang="scss" scoped>
@use './style/generals.scss';
</style>