<template>
    <Menu/>
    <slot/>
    <Footer/>
</template>

<script>
import Menu from "../Components/Menu";
import Footer from "../Components/Footer";
export default {
    components:{
        Menu,
        Footer,
    }
}
</script>

<style>

</style>