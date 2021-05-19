<template>
    <section id="sec2_container">
        <div id="sec2_div">
            <div class="left">
                <img src="images/pictures/image10.jpg" alt="" />
                <div class="topbottom_container">
                    <div class="top">
                        <span>BeGI é para todas</span>
                        <h3>BeGI Revolution: <br />Você única</h3>
                        <p>
                            Quem manda na minha terra sou euzis! Nec orci ornare
                            consequat. Praesent lacinia ultrices consectetur.
                            Sed non ipsum felis. Per aumento de cachacis, eu
                            reclamis. Admodum accumsan disputationi eu sit. Vide
                            electram sadipscing et per.
                        </p>
                    </div>
                    <div class="bottom">
                        <inertia-link>Ver Catálogo</inertia-link>
                    </div>
                </div>
            </div>

            <div class="right">
                <SwipBan />
            </div>
        </div>
    </section>
</template>

<script>
import SwipBanner from "./Swiper/SwipBanner";
export default {
    components: {
        SwipBan: SwipBanner,
    },
};
</script>

<style lang="scss">
@import "resources/css/sass/allImports";

#sec2_container {
    #sec2_div {
        // display: flex;

        background-color: $notblack;

        padding: 2vw 2vw 2vw 4vw;
        margin: 0 12vw 14vw 0;

        .left {
            display: flex;

            width: 50vw;

            img {
                width: 20vw;
            }
            .topbottom_container {
                display: flex;
                flex-direction: column;
                justify-content: space-between;

                margin-left: 2vw;

                .top {
                    span,
                    h3,
                    p {
                        color: $white;
                    }
                    span {
                        @include Font3_SI();
                        font-size: 1vw;
                    }
                    h3 {
                        @include Font1_S();
                        font-size: 3vw;
                    }
                    p {
                        @include Font2_SS();
                        font-size: 1.4vw;
                        margin-top: 1vw;
                    }
                }
                .bottom {
                    background-color: $black;
                    border-radius: 0.4vw;
                    width: fit-content;

                    margin: 0 0 1.5vw 1vw;
                    padding: 0.6vw 1.5vw 0.6vw 1.5vw;

                    transition-property: background-color;
                    transition-duration: 500ms;

                    &:hover{
                        background-color: $redwhite;
                        
                    }
                    &:hover a{
                        color: $black
                    }

                    a {
                        @include Font2_SS();
                        font-size: 1.4vw;
                        color: $white;
                    
                        transition-property: color;
                        transition-duration: 300ms;
                    }
                }
            }
        }
        .right {
            position: absolute;
        }
    }
}
</style>
