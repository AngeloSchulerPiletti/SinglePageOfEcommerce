<template>
    <nav>
        <div class="left">
            <inertia-link><LogoRose /></inertia-link>
        </div>
        <div class="center">
            <ul id="menu_links">
                <li><inertia-link>ROUPAS</inertia-link></li>
                <li><inertia-link>ACESSÓRIOS</inertia-link></li>
                <li><inertia-link>JOIAS</inertia-link></li>
                <li><inertia-link>CONTATO</inertia-link></li>
                <li><inertia-link>SOBRE NÓS</inertia-link></li>
            </ul>
        </div>
        <div class="right">
            <inertia-link><Search class="icons"/></inertia-link>
            <inertia-link><User class="icons"/></inertia-link>
            <inertia-link><Cart class="icons"/></inertia-link>
        </div>
    </nav>
</template>

<script>
import LogoRose from "../SVGs/LogoRose";

import Cart from "../SVGs/Cart";
import User from "../SVGs/User";
import Search from "../SVGs/Search";
export default {
    components: {
        LogoRose,
        Cart,
        User,
        Search,
    },
};
</script>

<style lang="scss" scoped>
@import "resources/css/sass/allImports";

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 1vw 0 1vw;

    background-color: $black;

    transition-property: padding;
    transition-duration: 200ms;

    &:hover {
        padding: 0.6vw 1vw 0.6vw 1vw;
    }

    .left {
        width: 12vw;
    }
    .center {
        #menu_links {
            li {
                display: inline-block;
                margin: 0 1.2vw 0 1.2vw;

                a {
                    @include Font2_SS();
                    color: $white;
                    font-size: 1.2vw;

                    transition-property: color;
                    transition-duration: 300ms;

                    &:hover {
                        color: $redwhite;
                    }
                }
            }
        }
    }
    .right{
      display: flex;
      justify-content: space-between;

      width: 6vw;

      .icons{
        width: 1.5vw;
        height: 1.5vw;
      }
    }
}
</style>
