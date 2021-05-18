<template>
    <section>
        <div>
            <div>
                <img src="" alt="" />
                <div>
                    <span></span>
                    <h3></h3>
                    <p></p>
                    <inertia-link></inertia-link>
                </div>
            </div>

            <div>
                <SwipBan/>
            </div>
        </div>
    </section>
</template>

<script>
import SwipBanner from "./Swiper/SwipBanner";
export default {
    components: {
        SwipBan: SwipBanner,
    },
};
</script>

<style></style>
