<script>
export default {
    name: "AppNav",

    data() {
        return {
            links: ["Characters", "Comics", "Movies", "Tv", "Games", "Collectibles", "Videos", "Fans", "News", "Shop"],

            activeLinkIndex: 1,

        }


    }
}


</script>

<template>
    <nav>
        <div class="container">

            <div>
                <img src="/img/dc-logo.png" alt="">
            </div>
            <div>
                <ul>
                    <li v-for="(link, index) in links" :class="index == activeLinkIndex ? 'active' : ''">

                        <a href=""> {{ link }}</a>
                    </li>
                </ul>
            </div>

        </div>

    </nav>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixin' as *;


.container {

    @include centered;

    display: flex;
    justify-content: space-between;
    align-items: center;

    img {
        height: 80px;
    }


    ul {
        display: flex;
        gap: 2em;
        text-transform: uppercase;
        font-weight: bold;


        li {
            position: relative;
            display: flex;
            align-items: center;
            height: 120px;


            a {
                color: inherit;
                text-decoration: none;
            }

            &.active {
                color: $primaryColor;
            }

            &.active::before {
                content: '';
                position: absolute;
                bottom: 0;
                left: 0;

                width: 100%;
                height: 4px;


                background-color: $primaryColor;
            }


        }


    }

}
</style>
