<template>
    <section>
        <SwipCar/>
    </section>
</template>

<script>
import SwipCarousel from "./Swiper/SwipCarousel";
export default {
    components:{
        SwipCar: SwipCarousel,
    },
    props:{
        // scrollData: Object,
    }
}
</script>

<style>

</style>