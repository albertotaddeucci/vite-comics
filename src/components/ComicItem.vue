<script>

export default {
    name: "ComicItem",

    props: {
        comicImage: String,
        comicTitle: String,
    }

}


</script>


<template>
    <div class="comic">
        <img :src="comicImage" :alt="comicTitle">
        <span>{{ comicTitle }}</span>
    </div>
</template>

<style lang="scss">
@use '../styles/mixin' as *;

.comic {
    width: calc(100% / 6 - 30px * 6 / 5);

    img {
        max-width: 185px;
        height: 185px;
        width: 100%;

        margin-bottom: 10px;

        object-fit: cover;
        object-position: 0px 0px;
    }



    span {
        color: white;
        text-transform: uppercase;
        font-size: 14px;

    }
}
</style>