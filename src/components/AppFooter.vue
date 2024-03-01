<script>
import { toValue } from 'vue';

export default {
    name: "AppFooter",

    data() {
        return {
            lists: [
                {
                    title: "Dc comics",
                    links: ["Characters", "Comics", "Movies", "Tv", "Games", "Videos", "News"]
                },
                {
                    title: "Shop",
                    links: ["Shop DC", "Shop DC Collection"]
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


            ]
        }
    }
}


</script>

<template>
    <footer>

        <div class="wrapper">

            <div class="link-lists">

                <div v-for="list in lists" class="lists">
                    <h3>{{ list.title }}</h3>
                    <ul>
                        <li v-for="currentLink in list.links">{{ currentLink }}</li>


                    </ul>


                </div>
            </div>


            <div>

                <img id="logo-bg" src="/img/dc-logo-bg.png" alt="">
            </div>


        </div>


    </footer>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixin' as *;


footer {
    // position: relative;

    background-image: url(/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    color: white;
    height: 370px;
    overflow: hidden;



    .wrapper {
        @include centered;

        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
        padding-block: 40px;

        font-size: 14px;


        .link-lists {
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            align-content: flex-start;
            gap: 20px;

            height: 100%;
        }




        .lists {


            line-height: 20px;

            h3 {
                margin-bottom: 16px;

                text-transform: uppercase;
                font-size: 18px;
            }

            ul {
                list-style-type: none;

                li {
                    color: $secondaryColor;

                    &:hover {
                        color: white;
                        cursor: pointer;
                    }
                }
            }



        }
    }




}
</style>