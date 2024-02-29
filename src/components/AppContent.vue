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

<style>
#content {

    background-color: black;
    color: white;

    .wrapper {
        max-width: 1260px;
        margin-inline: auto;

        div {
            padding-block: 30px;
        }
    }

}
</style>
