<template>
    <div :class="layout">
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
                <button @click="searchField()"><Search class="icons" /></button>
                <inertia-link><User class="icons" /></inertia-link>
                <inertia-link><Cart class="icons" /></inertia-link>
            </div>
        </nav>
        <div
            id="search_container"
            data-searchstate="none"
            style="display: none"
        >
            <form action="busca" method="get">
                <input type="text" name="search" id="searchInput" />
                <button type="submit" id="searchButton">
                    <Search id="searchIcon" />
                </button>
            </form>
        </div>
    </div>
</template>

<script>
import LogoRose from "../SVGs/LogoRose";

import Cart from "../SVGs/Cart";
import User from "../SVGs/User";
import Search from "../SVGs/Search";
export default {
    data() {
        return {
            searchFieldState: false,
        };
    },
    methods: {
        searchField() {
            var state = this.searchFieldState,
                searchButton = document.querySelector("#search_container");

            if (state) {
                searchButton.dataset.searchstate = "hide";
                searchButton.style.display = "none";

                this.$data.searchFieldState = false;
            } else {
                searchButton.style.display = "block";
                searchButton.dataset.searchstate = "show";

                this.$data.searchFieldState = true;
            }
        },
    },
    components: {
        LogoRose,
        Cart,
        User,
        Search,
    },
    props:{
        layout: String,
    }
};
</script>

<style lang="scss" scoped>
@import "resources/css/sass/allImports";
@import "resources/css/sass/components/Menu/mixins";


.block {
    transform-style: preserve-3d;

    nav {
        display: grid;
        grid-template-columns: 4fr 9fr 4fr;
        justify-items: center;
        align-items: center;

        padding: 0 1vw 0 1vw;
        background-color: $black;

        z-index: 100;

        .left {
            width: 12vw;
        }
        .center {
            #menu_links {
                li {
                    display: inline-block;
                    margin: 0 1.2vw 0 1.2vw;

                    @include anchor();
                }
            }
        }
        .right {
            display: flex;
            justify-content: space-between;

            width: 6vw;

            .icons {
                width: 1.5vw;
                height: 1.5vw;
            }
            button {
                background-color: transparent;
                border: none;
                cursor: pointer;
            }
        }
    }

    #search_container {
        padding: 0.7vw 1vw 0.4vw 1vw;

        background-color: $notblack;

        form {
            display: grid;
            grid-template-columns: 18fr 1fr;
            grid-template-rows: 2.4vw;

            width: 100%;
            height: 100%;

            #searchInput {
                flex-grow: 1;

                background-color: transparent;
                border: none;
                border-bottom: 1px solid $white;

                @include Font2_SS();
                font-size: 1.4vw;
                color: $notwhite;
            }
            #searchButton {
                background-color: transparent;
                border: none;

                cursor: pointer;

                #searchIcon {
                    width: 2vw;
                    height: 2vw;
                }
            }
        }
    }
}
.fixed{
    position: fixed;
    left: 0;
    right: 0;


    nav {
        text-align: center;

        padding: 1vw 1vw 1vw 1vw;
        background-color: $black;

        z-index: 100;

        .left {
            display: none;
        }
        .center {
            #menu_links {
                li {
                    display: inline-block;
                    margin: 0 2vw 0 2vw;

                    @include anchor();
                }
            }
        }
        .right {
            display: none;
        }
    }

    #search_container {
        padding: 0.7vw 1vw 0.4vw 1vw;

        background-color: $notblack;

        form {
            display: grid;
            grid-template-columns: 18fr 1fr;
            grid-template-rows: 2.4vw;

            width: 100%;
            height: 100%;

            #searchInput {
                flex-grow: 1;

                background-color: transparent;
                border: none;
                border-bottom: 1px solid $white;

                @include Font2_SS();
                font-size: 1.4vw;
                color: $notwhite;
            }
            #searchButton {
                background-color: transparent;
                border: none;

                cursor: pointer;

                #searchIcon {
                    width: 2vw;
                    height: 2vw;
                }
            }
        }
    }
}

// [data-searchState] {
// //
// }
[data-searchState="none"] {
    transform: translateY(-100%) translateZ(-1vw);
    opacity: 0;
}
[data-searchState="hide"] {
    transform: translateY(-100%) translateZ(-1vw);
    opacity: 0;
}
[data-searchState="show"] {
    transform: translateY(0) translateZ(-1vw);
    opacity: 1;
}
</style>
