<template>
    <Menu/>
    <slot/>
    <Footer/>
</template>

<script>
import Menu from "../Components/AppLayout/Menu";
import Footer from "../Components/AppLayout/Footer";
export default {
    components:{
        Menu,
        Footer,
    }
}
</script>

<style>

</style>