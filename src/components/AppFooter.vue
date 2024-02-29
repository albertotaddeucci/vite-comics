<script>
import { toValue } from 'vue';

export default {
    name: "AppFooter",

    data() {
        return {
            lists: [
                {
                    title: "Dc comics",
                    links: ["", "", "Movies", "Tv", "Games", "Videos", "News"]
                },
                {
                    title: "Dc",
                    links: ["Terms Of Use", "Privacy Policy (New)",
                        "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates",
                        "Raitings", "Shop Help", "Contact Us"]
                },

                {
                    title: "Sites",
                    links: ["DC", "MAD Magazine", "DC Kinds", "DC Universe", "DC Power Visa"]
                },
                {
                    title: "Shop",
                    links: ["Shop DC", "Shop DC Collection"]
                },


            ]
        }
    }
}


</script>

<template>
    <footer>

        <div class="wrapper">

            <div>
                <div class="lists">
                    <h3>DC COMICS</h3>
                    <ul>
                        <li>Characters</li>
                        <li>Comics</li>
                        <li>Movies</li>
                        <li>Tv</li>
                        <li>Games</li>
                        <li>Videos</li>
                        <li>News</li>

                    </ul>


                </div>
                <div class="lists">
                    <h3>SHOP</h3>
                    <ul>
                        <li>Shop DC</li>
                        <li>Shop DC Collectibles</li>

                    </ul>


                </div>

            </div>
            <div class="lists">
                <h3>DC</h3>
                <ul>
                    <li>Terms Of Use</li>
                    <li>Privacy Policy (New)</li>
                    <li>Ad Choices</li>
                    <li>Advertising</li>
                    <li>Jobs</li>
                    <li>Subscriptions</li>
                    <li>Talent Workshop</li>
                    <li>CPSC Certificates</li>
                    <li>Raitings</li>
                    <li>Shop Help</li>
                    <li>Contact Us</li>

                </ul>


            </div>
            <div class="lists">
                <h3>SITES</h3>
                <ul>
                    <li>DC</li>
                    <li>MAD Magazine</li>
                    <li>DC KIds</li>
                    <li>DC Universe</li>
                    <li>DC Power Visa</li>


                </ul>


            </div>



        </div>

        <img id="logo-bg" src="/img/dc-logo-bg.png" alt="">

    </footer>
</template>

<style lang="scss">
@use '../styles/variables' as *;

footer {
    background-image: url(/img/footer-bg.jpg);

    color: white;

    position: relative;

    .wrapper {
        max-width: 1260px;
        margin-inline: auto;
        display: flex;
        gap: 20px;

        padding-block: 40px;
        font-size: 12px;



        .lists {
            display: flex;
            flex-direction: column;

            h3 {
                font-size: 16px;
                margin-bottom: 20px;
            }

            ul {
                list-style-type: none;
                padding-bottom: 20px;
            }



        }
    }

    #logo-bg {
        position: absolute;
        top: -100px;
        right: 0;
    }


}
</style>