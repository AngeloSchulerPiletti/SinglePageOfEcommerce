<template>
    <div id="_website_container_">
        <Menu id="menu"/>
        <slot />
        <Footer id="rodape"/>
    </div>
</template>

<script>
import Menu from "../Components/AppLayout/Menu";
import Footer from "../Components/AppLayout/Footer";
export default {
    components: {
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
    display: flex;
    flex-direction: column;
    height: 100vh;
    background-color: $redwhite;

    #rodape{
        margin-top: auto;
    }
}
</style>
