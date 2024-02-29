<script>
export default {
    name: "AppCards",

    data() {
        return {
            cards: [
                {
                    image: '/img/buy-comics-digital-comics.png',
                    text: "Digital Comics"

                },
                {
                    image: '/img/buy-comics-merchandise.png',
                    text: "DC Mechandise"

                },
                {
                    image: '/img/buy-comics-subscriptions.png',
                    text: "Subscription"

                },
                {
                    image: '/img/buy-comics-shop-locator.png',
                    text: "Comic Shop Locator"

                },
                {
                    image: '/img/buy-dc-power-visa.svg',
                    text: "DC Power visa"

                },
            ]
        }
    }


}


</script>

<template>
    <div id="cards">
        <div class="wrapper">
            <div v-for="card in cards" class="card">
                <div>
                    <img :src="card.image" alt="">
                </div>
                <div>
                    {{ card.text }}
                </div>

            </div>
        </div>
    </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixin' as *;


#cards {
    background-color: $primaryColor;
    color: white;

    position: relative;
    z-index: 2;

    .wrapper {
        @include centered;
        display: flex;
        justify-content: space-around;

        .card {
            padding: 40px;
            display: flex;
            align-items: center;
            gap: 15px;
            font-size: 12px;
            text-transform: uppercase;

            img {
                width: 50px;
            }

            &:hover {
                cursor: pointer;
            }
        }
    }
}
</style>
