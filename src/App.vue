<script>

import AppNav from './components/AppNav.vue';
import AppContent from './components/AppContent.vue';
import AppFooter from './components/AppFooter.vue';
import AppFooterBottom from './components/AppFooterBottom.vue'

export default {
  components: {
    AppNav,
    AppContent,
    AppFooter,
    AppFooterBottom,
  }
}


</script>

<template>
  <AppNav></AppNav>

  <AppContent></AppContent>



  <AppFooter></AppFooter>

  <AppFooterBottom></AppFooterBottom>
</template>

<style></style>
