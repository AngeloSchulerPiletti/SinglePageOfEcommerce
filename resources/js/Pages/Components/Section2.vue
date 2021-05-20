<template>
    <section :class="'sec2_container '+state+'_container'">
        <div id="sec2_div" :class="state+'_left'">
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

            <div :class="'right '+state+'_right'">
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
    props:{
        state: String,
    },
};
</script>

<style lang="scss" scoped>
@import "resources/css/sass/allImports";





//+----------------------------------------+
//|             ESTILO GERAL               |
//+----------------------------------------+

.sec2_container {
    #sec2_div {
        display: flex;

        position: relative;

        background-color: $notblack;

        padding: 3vw 3vw 3vw 5vw;
        margin: 0 18vw 14vw 0;

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
            right: 0;
            top: 50%;

            transform: translate(40%, -50%);           
        }
    }
}





//+----------------------------------------+
//|                ANIMAÇÕES               |
//+----------------------------------------+
@include section2_anim();

.none_container{
    opacity: 0;
}
.show_container{
    opacity: 1;
}




.none_left{
    opacity: 0;
}
.hide_left{
    animation: hiding_left 300ms ease-out 000ms 1 normal both;
}
.show_left{
    animation: showing_left 300ms ease-out 0ms 1 normal both;
}

.none_right{
    opacity: 0;
}
.hide_right{
    animation: hiding_right 200ms ease-out 0ms 1 normal both;
     
}
.show_right{
    animation: showing_right 400ms ease-out 600ms 1 normal both;
     
}









//+----------------------------------------+
//|            RESPONSIVIDADE              |
//+----------------------------------------+
@media (max-width: 800px){
    
}
@media (max-width: 600px){

}
@media (max-width: 500px){

}
@media (max-width: 350px){

}
</style>
