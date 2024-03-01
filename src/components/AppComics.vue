<script>
import jsonData from './data/dc-comics.json'

import ComicItem from './ComicItem.vue';

export default {
    name: "AppComics",



    data() {
        return {
            comicItems: jsonData,
        }
    },

    components: { ComicItem },


}


</script>


<template>
    <div class="comics-container">

        <div class="comics">
            <div class="current">
                <span>CURRENT SERIES</span>
            </div>

            <ComicItem v-for="comic in comicItems" :comicImage="comic.thumb" :comicTitle="comic.series"></ComicItem>

        </div>
        <button>Load More</button>
    </div>
</template>

<style lang="scss">
@use '../styles/mixin' as *;
@use '../styles/variables' as *;

.current {
    position: absolute;
    top: -60px;
    left: 0;

    span {
        padding: 14px 30px;
        background-color: $primaryColor;
        color: white;
        font-weight: bold;
        font-size: 22px;

    }
}

.comics-container {


    padding-top: 50px;
    padding-bottom: 20px;

    background-color: $bgColor ;

    button {
        display: block;
        margin: 0 auto;

        @include btn-secondary($primaryColor)
    }

}

.comics {
    position: relative;
    @include centered;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 30px;

    padding-bottom: 40px;

}
</style>