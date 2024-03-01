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
        <div>

        </div>
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
        padding-bottom: 20px;
        width: 100%;
        object-fit: cover;
    }



    span {
        color: white;
        text-transform: uppercase;
        font-size: 14px;

    }
}
</style>