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
                        {{ link }}
                    </li>
                </ul>
            </div>

        </div>

    </nav>
</template>

<style>
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;

    max-width: 1260px;
    margin-inline: auto;
    padding-block: 20px;

    ul {
        display: flex;
        gap: 2em;

        list-style: none;
        text-transform: uppercase;
    }

}
</style>
