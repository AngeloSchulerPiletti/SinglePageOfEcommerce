<template>
    <section>
        <div id="sec1_container">
            <div id="sec1_left">
                <div>
                    <span>BeGI é ser você</span>
                    <h3>Ser linda nunca foi tão fácil</h3>
                    <p>Mussum Ipsum, cacilds vidis litro abertis. Praesent vel viverra nisi. Mauris 
                        aliquet nunc non turpis scelerisque, eget. Casamentiss faiz malandris se 
                        pirulitá. Per aumento de cachacis, eu reclamis. A ordem dos tratores não altera 
                        o pão duris.</p>
                </div>
                <img src="" alt="" />
            </div>

            <div id="sec1_right">
                <div class="div_left card_container">
                    <img src="images/pictures/image1.jpg" alt="" />
                    <div>
                        <h6>Linha Dark Girls</h6>
                        <p>A renovada linha gótica que perpassa a história da humanidade. BeGI, BeGothic</p>
                    </div>
                </div>

                <div class="div_right">
                    <div class="card_container">
                        <img src="images/pictures/image4.jpg" alt="" />
                        <div>
                            <h6>Linha Sad Girls:BeSad</h6>
                            <p>BeGI, BeSad... A beleza é conveniente até mesmo na tristeza</p>
                        </div>
                    </div>
                    <div class="card_container">
                        <img src="images/pictures/image2.jpg" alt="" />
                        <div>
                            <h6>Linha Make:BePowder</h6>
                            <p>Porque maquiagem nunca é demais para você</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import 'resources/css/sass/allImports';


#sec1_container{
    display: flex;
    background-color: $notblack;
    margin: 0 0vw 34vw 0;
    

    // position: relative;
    // height: 50%;
    // width: 100%;

    padding: 2vw 2vw 20vw 2vw;
    
    justify-content: space-between;
    align-items: flex-start;
    
    #sec1_left{
        width: 38vw;
        margin-right: 5vw;
        margin-top: 6vw;

        div{
            
            span, h3, p{
                color: $notwhite;
            }
            span{
                @include Font3_SI();
                font-size: 1vw
            }
            h3{
                @include Font1_S();
                font-size: 3vw
            }
            p{
                @include Font2_SS();
                font-size: 1.4vw;
                margin-top: 1vw;
            }
        }
    }
    #sec1_right{
        width: 64vw;

        
        h6, p{
            color: $notwhite;
            padding: 0 2vw 0 2vw;
            
        }
        h6{
            @include Font2_S();
            font-size: 1.5vw;
            margin-top: 1vw;
            margin-bottom: 0.4vw;

        }
        p{
            @include Font2_SSI();
            font-size: 1vw;
        }

        .div_left{
            position: absolute;
            transform: translateY(10%);
            width: 28vw;
            img{
                width: 100%;
            }
        }
        .div_right{
            position: absolute;

            right: 0vw;

            width: 28vw;
            img{
                width: 100%;
            }
        }
        .card_container{
            margin: 0vw 2vw 2.5vw 0;
            padding: 0 0 1.6vw 0;
            text-align: center;
            background-color: $black;

            height: fit-content;
        }
    }
}
</style>
