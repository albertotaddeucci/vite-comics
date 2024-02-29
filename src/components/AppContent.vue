<script>
import AppCards from './AppCards.vue';

export default {
    name: "AppContent",
    components: { AppCards }


}


</script>

<template>
    <div id="content">
        <div class="wrapper">
            <div>
                content
            </div>
        </div>
    </div>
    <AppCards></AppCards>
</template>

<style = lang="scss">
@use '../styles/mixin' as *;

#content {

    background-color: black;
    color: white;

    .wrapper {

        @include centered;

        div {
            padding-block: 30px;
        }
    }

}
</style>
