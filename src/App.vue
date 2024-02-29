<script>

import AppNav from './components/AppNav.vue';
import AppCards from './components/AppCards.vue';
import AppContent from './components/AppContent.vue';
import AppFooter from './components/AppFooter.vue';
import AppFooterBottom from './components/AppFooterBottom.vue'

export default {
  components: {
    AppNav,
    AppContent,
    AppCards,
    AppFooter,
    AppFooterBottom,
  }
}


</script>

<template>
  <AppNav></AppNav>

  <AppContent></AppContent>

  <AppCards></AppCards>


  <AppFooter></AppFooter>

  <AppFooterBottom></AppFooterBottom>
</template>

<style></style>
