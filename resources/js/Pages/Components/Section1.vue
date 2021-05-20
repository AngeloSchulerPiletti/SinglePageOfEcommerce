<template>
    <section :class="state + '_container'">
        <div class="sec1_container" :class="state + '_left'">
            <div id="sec1_left">
                <div class="top_container">
                    <span>BeGI é ser você</span>
                    <h3>Ser linda nunca foi tão fácil</h3>
                    <p>
                        Mussum Ipsum, cacilds vidis litro abertis. Praesent vel
                        viverra nisi. Mauris aliquet nunc non turpis
                        scelerisque, eget. Casamentiss faiz malandris se
                        pirulitá. Per aumento de cachacis, eu reclamis. A ordem
                        dos tratores não altera o pão duris.
                    </p>
                </div>
                <div class="bottom_container">
                    <Arrow id="arrow" :class="state+'_arrow'"/>
                </div>
            </div>

            <div id="sec1_right" :class="state + '_right'">
                <div class="div_left">
                    <div
                        class="card_container"
                        id="card1"
                        @mouseover="showP(1)"
                        @mouseleave="hideP(1)"
                    >
                        <img src="images/pictures/image1.jpg" alt="" />
                        <div>
                            <h6>Linha Dark Girls</h6>
                            <p>
                                A renovada linha gótica que perpassa a história
                                da humanidade. BeGI, BeGothic
                            </p>
                        </div>
                        <div
                            id="toAbove1"
                            data-state="none"
                            style="display: none"
                        >
                            <h6>Linha Dark Girls</h6>
                            <p>
                                A renovada linha gótica que perpassa a história
                                da humanidade. BeGI, BeGothic
                            </p>
                            <p id="show_p1">
                                Mussum Ipsum, cacilds vidis litro abertis. Mais
                                vale um bebadis conhecidiss, que um alcoolatra
                                anonimis. Diuretics paradis num copo é motivis
                                de denguis. Praesent vel viverra nisi. Mauris
                                aliquet nunc non turpis scelerisque, eget. Em pé
                                sem cair, deitado sem dormir, sentado sem
                                cochilar e fazendo pose. Quem manda na minha
                                terra sou euzis! Nec orci ornare consequat.
                                Praesent lacinia ultrices consectetur. Sed non
                                ipsum felis. Per aumento de cachacis, eu
                                reclamis. Admodum accumsan disputationi eu sit.
                                Vide electram sadipscing et per.
                            </p>
                        </div>
                    </div>
                </div>

                <div class="div_right">
                    <div
                        class="card_container"
                        id="card2"
                        @mouseover="showP(2)"
                        @mouseleave="hideP(2)"
                    >
                        <img src="images/pictures/image4.jpg" alt="" />
                        <div>
                            <h6>Linha Sad Girls:BeSad</h6>
                            <p>
                                BeGI, BeSad... A beleza é conveniente até mesmo
                                na tristeza
                            </p>
                        </div>
                        <div
                            id="toAbove2"
                            data-state="none"
                            style="display: none"
                        >
                            <h6>Linha Sad Girls:BeSad</h6>
                            <p>
                                BeGI, BeSad... A beleza é conveniente até mesmo
                                na tristeza
                            </p>
                            <p id="show_p2">
                                Mussum Ipsum, cacilds vidis litro abertis. Mais
                                vale um bebadis conhecidiss, que um alcoolatra
                                anonimis. Diuretics paradis num copo é motivis
                                de denguis. Praesent vel viverra nisi. Mauris
                                aliquet nunc non turpis scelerisque, eget.
                            </p>
                        </div>
                    </div>
                    <div
                        class="card_container"
                        id="card3"
                        @mouseover="showP(3)"
                        @mouseleave="hideP(3)"
                    >
                        <img src="images/pictures/image2.jpg" alt="" />
                        <div>
                            <h6>Linha Make:BePowder</h6>
                            <p>Porque maquiagem nunca é demais para você</p>
                        </div>
                        <div
                            id="toAbove3"
                            data-state="none"
                            style="display: none"
                        >
                            <h6>Linha Make:BePowder</h6>
                            <p>Porque maquiagem nunca é demais para você</p>
                            <p id="show_p3">
                                Mussum Ipsum, cacilds vidis litro abertis. Mais
                                vale um bebadis conhecidiss, que um alcoolatra
                                anonimis. Diuretics paradis num copo é motivis
                                de denguis. Praesent vel viverra nisi. Mauris
                                aliquet nunc non turpis scelerisque, eget. Em pé
                                sem cair, deitado sem dormir, sentado sem
                                cochilar e fazendo pose. Quem manda na minha
                                terra sou euzis! Nec orci ornare consequat.
                                Praesent lacinia ultrices consectetur. Sed non
                                ipsum felis. Per aumento de cachacis, eu
                                reclamis. Admodum accumsan disputationi eu sit.
                                Vide electram sadipscing et per.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import Arrow from "./SVGs/Arrow";
export default {
    methods: {
        showP: function (el) {
            var elementAbove = document.querySelector("#toAbove" + el),
                elementCard = document.querySelector("#card" + el);

            elementAbove.style.display = "block";
            elementAbove.dataset.state = "show";
        },
        hideP: function (el) {
            var elementAbove = document.querySelector("#toAbove" + el),
                elementCard = document.querySelector("#card" + el);

            elementAbove.dataset.state = "hide";
            setTimeout(function () {
                elementAbove.style.display = "none";
            }, 600);
        },
    },
    props: {
        state: String,
    },
    components: {
        Arrow,
    },
};
</script>

<style lang="scss">
@import "resources/css/sass/allImports";

.sec1_container {
    display: flex;
    background-color: $notblack;
    margin: 0 0vw 34vw 0;

    padding: 2vw 2vw 20vw 2vw;

    justify-content: space-between;
    align-items: flex-start;

    #sec1_left {
        width: 38vw;
        margin-right: 5vw;
        margin-top: 6vw;

        .top_container {
            span,
            h3,
            p {
                color: $notwhite;
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
        .bottom_container {
            position: relative;

            width: 10vw;
            height: 10vw;

            #arrow {
                position: absolute;

                top: 0;
                left: 0;

                transform: translate(100%, 350%);

                width: 100%;
                height: 100%;

            }
        }
    }
    #sec1_right {
        width: 64vw;

        h6,
        p {
            color: $notwhite;
            padding: 0 2vw 0 2vw;
        }
        h6 {
            @include Font2_S();
            font-size: 1.5vw;
            margin-top: 1vw;
            margin-bottom: 0.4vw;
        }
        p {
            @include Font2_SSI();
            font-size: 1vw;
        }

        .div_left {
            position: absolute;
            transform: translateY(10%);
            width: 28vw;
            img {
                width: 100%;
            }
        }
        .div_right {
            position: absolute;

            right: 0;

            width: 28vw;
            img {
                width: 100%;
            }
        }
        .card_container {
            position: relative;

            margin: 0vw 2vw 2.5vw 0;
            padding: 0 0 1.6vw 0;
            text-align: center;
            background-color: $black;

            height: fit-content;
        }

        @import "resources/css/sass/components/Section2/animations";
        [data-state="show"] {
            position: absolute;

            padding-top: 5%;
            top: 0;
            bottom: 0;

            animation: showAnim 500ms ease-out 0ms 1 normal both;
        }
        [data-state="hide"] {
            position: absolute;

            padding-top: 5%;
            top: 0;
            bottom: 0;

            animation: hideAnim 500ms ease-in 0ms 1 normal both;
        }
    }
}

@include section1_anim();

.none_container {
    opacity: 0;
}
.show_container {
    opacity: 1;
}

.none_left {
    opacity: 0;
}
// .hide_left{
//     animation: hiding_left 500ms ease-out 200ms 1 normal both;
// }
.show_left {
    animation: showing_left 600ms ease-out 0ms 1 normal both;
}

.none_right {
    opacity: 0;
}
// .hide_rigth{
//     animation: hiding_right 200ms ease-out 0ms 1 normal both;
// }
.show_right {
    animation: showing_right 400ms ease-out 600ms 1 normal both;
}

.none_arrow{
    //
}
.show_arrow{
    animation: showing_arrow 1200ms linear 2000ms 5 normal both;
}
</style>
