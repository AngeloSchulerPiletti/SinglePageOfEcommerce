<template>
    <div>
        <aside id="menu_side">
            <div class="left">
                <ul id="menu_links">
                    <li><inertia-link>ROUPAS</inertia-link></li>
                    <li><inertia-link>ACESSÓRIOS</inertia-link></li>
                    <li><inertia-link>JOIAS</inertia-link></li>
                    <li><inertia-link>CONTATO</inertia-link></li>
                    <li><inertia-link>SOBRE NÓS</inertia-link></li>
                </ul>
            </div>
            <div class="right">
                <Arrow id="pushIcon" />
            </div>
        </aside>
    </div>
</template>

<script>
import Arrow from "../SVGs/Arrow";
export default {
    components:{
        Arrow,
    }
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

        .left,
        .right {
            background-color: $notblack;
        }
        .left {
            width: 30vw;
        }
        .right {
            #pushIcon {
                width: 6vw;
            }
        }
    }
}
@media (max-width: 350px) {
}
</style>
