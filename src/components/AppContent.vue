<script>
import AppCards from './AppCards.vue';
import AppComics from './AppComics.vue';

export default {
    name: "AppContent",
    components: { AppCards, AppComics }

}


</script>

<template>
    <div id="jumbo"></div>

    <AppComics></AppComics>

    <AppCards></AppCards>
</template>

<style lang="scss">
@use '../styles/mixin' as *;

#jumbo {

    background-image: url(/img/jumbotron.jpg);
    background-size: cover;
    height: 400px;
    color: white;

}
</style>
