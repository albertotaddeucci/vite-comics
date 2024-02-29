<script>
export default {
    name: "AppNav",

    data() {
        return {
            links: ["Characters", "Comics", "Movies", "Tv", "Games", "Collectibles", "Videos", "Fans", "News", "Shop"]
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
                    <li v-for="link in links">
                        <a href="">{{ link }}</a>
                    </li>
                </ul>
            </div>

        </div>

    </nav>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixin' as *;
// 


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

        list-style: none;
        text-transform: uppercase;

        li {

            padding-block: 50px;

        }


        a {
            padding-block: 47px;

            font-size: 12px;
            font-weight: bold;
            text-decoration: none;

            &.active {
                color: $primaryColor;
                border-bottom: 5px solid $primaryColor;

            }

            &:hover {
                color: $primaryColor;
                cursor: pointer;

                border-bottom: 5px solid $primaryColor;

            }

        }

    }

}
</style>
