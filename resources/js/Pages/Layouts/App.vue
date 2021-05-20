<template>
    <div id="_website_container_">
        <Menu id="menu" :layout="menuLayout" />
        <SideMenu id="sidemenu" />
        <slot id="slot" />
        <Footer id="rodape" />
    </div>
</template>

<script>
import SideMenu from "../Components/AppLayout/SideMenu";
import Menu from "../Components/AppLayout/Menu";
import Footer from "../Components/AppLayout/Footer";
export default {
    data() {
        return {
            menuLayout: "block",
        };
    },
    created() {
        window.addEventListener("scroll", this.handleScroll);
    },
    destroyed() {
        window.removeEventListener("scroll", this.handleScroll);
    },
    methods: {
        handleScroll(event) {
            var scrollDelta = document.documentElement.scrollHeight,
                scrollY = document.documentElement.scrollTop,
                windowHeight = window.innerHeight;

            console.log(scrollY);
            if (scrollY > 30) {
                this.$data.menuLayout = "fixed";
            } else {
                this.$data.menuLayout = "block";
            }
        },
    },
    components: {
        SideMenu,
        Menu,
        Footer,
    },
};
</script>

<style lang="scss">
@import "resources/css/sass/allImports";

* {
    margin: 0;
    padding: 0;
    outline: 0;
    text-decoration: none;
    color: $black;
    @include Font2_SS;

    ul {
        li {
            list-style: none;
        }
    }
}

#_website_container_ {
    position: relative;

    display: flex;
    flex-direction: column;
    height: 100vh;
    background-color: $redwhite;

    #sidemenu {
        z-index: 1000;
    }

    #menu {
        z-index: 100000;
    }

    #slot {
        z-index: 1;
    }

    #rodape {
        margin-top: auto;
    }
}
</style>
