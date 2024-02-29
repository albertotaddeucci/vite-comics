<script>
export default {
    name: "AppContent",
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
