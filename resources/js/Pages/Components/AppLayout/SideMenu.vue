<template>
    <div>
        <aside id="menu_side">
            <div class="left">
                <ul id="menu_links">
                    <li><inertia-link>ROUPAS</inertia-link></li>
                    <hr/>
                    <li><inertia-link>ACESSÓRIOS</inertia-link></li>
                    <hr/>
                    <li><inertia-link>JOIAS</inertia-link></li>
                    <hr/>
                    <li><inertia-link>CONTATO</inertia-link></li>
                    <hr/>
                    <li><inertia-link>SOBRE NÓS</inertia-link></li>
                    <hr/>
                </ul>
            </div>
            <div class="right">
                <button class="pushButton">
                    <Arrow2 id="pushIcon" />
                </button>
            </div>
        </aside>
    </div>
</template>

<script>
import Arrow2 from "../SVGs/Arrow2";
export default {
    components: {
        Arrow2,
    },
};
</script>

<style lang="scss" scoped>
@import "resources/css/sass/allImports";

//+----------------------------------------+
//|             ESTILO GERAL               |
//+----------------------------------------+
#menu_side {
    display: none;
}

//+----------------------------------------+
//|                ANIMAÇÕES               |
//+----------------------------------------+

//+----------------------------------------+
//|            RESPONSIVIDADE              |
//+----------------------------------------+
@media (max-width: 500px) {
    #menu_side {
        display: flex;

        position: fixed;

        top: 0;
        bottom: 0;
        left: 0;

        // transform: translateX(-77%);

        .left {
            padding-top: 14vw;
            width: 30vw;
            background-color: $black;

            z-index: 100;

            border-right: 1px solid $notwhite;
            #menu_links{
                li{
                    margin-left: 1vw;

                    font-size: 3vw;
                    a{
                        color: $white;
                    }
                }
                hr{
                    border: none;
                    outline: none;

                    height: 1px;
                    background-color: $notwhite;

                    margin: 1vw 0 1vw 0;
                }
            }
            
        }
        .right {
            padding-top: 18vw;

            z-index: 10;
            .pushButton {
                background-color: $black;
                border: none;
                cursor: pointer;

                height: 10vw;
                width: 10vw;

                padding: 1.5vw 1.5vw 1.5vw 2vw;

                border-radius: 0 1.5vw 1.5vw 0;

                transform: translateX(-3px);

                -webkit-tap-highlight-color: transparent;
                
                #pushIcon {
                    height: 100%;
                    width: 100%;
                    transform: rotateZ(-90deg);
                }
            }
        }
    }
}
@media (max-width: 350px) {
}
</style>
