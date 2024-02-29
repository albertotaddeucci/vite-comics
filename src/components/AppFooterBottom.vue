<script>
export default {
    name: "AppFooterBottom",


}


</script>

<template>
    <div id="footer-bottom">
        <div class="wrapper">


            <div>
                <button>SIGN-UP NOW!</button>
            </div>
            <div class="follow-us">
                <div>FOLLOW US</div>
                <div>
                    <img src="/img/footer-facebook.png" alt="">
                </div>
                <div>
                    <img src="/img/footer-twitter.png" alt="">
                </div>
                <div>
                    <img src="/img/footer-youtube.png" alt="">
                </div>
                <div>
                    <img src="/img/footer-pinterest.png" alt="">
                </div>
                <div>
                    <img src="/img/footer-periscope.png" alt="">
                </div>
            </div>
        </div>


    </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixin' as *;


#footer-bottom {
    position: relative;
    z-index: 2;
    background-color: #303030;

    .wrapper {

        @include centered;

        padding-block: 25px;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .follow-us {
            display: flex;
            align-items: center;
            gap: 10px;

            div:first-of-type {
                font-weight: bold;
                font-size: 20px;
                color: $primaryColor;
            }
        }
    }


    button {
        @include btn-primary($primaryColor)
    }
}
</style>