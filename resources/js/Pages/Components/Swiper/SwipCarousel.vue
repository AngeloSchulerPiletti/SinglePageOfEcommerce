<template>
    <div id="swiper_container">
        <swiper
            :spaceBetween="0"
            :centeredSlides="true"
            :autoplay="{
                delay: 2500,
                disableOnInteraction: false,
            }"
            id="swiper_carousel"
        >
            <swiper-slide
                class="slides"
                v-for="(image, index) in images"
                :key="index"
            >
                <img class="carousel_imgs" :src="image" alt="" />
            </swiper-slide>
        </swiper>
        <div id="carousel_selector">
            <div
                class="selector_container"
                v-for="(image, index) in images"
                :key="index"
            >
                <carouselbutton @click="goToImg(i)" />
            </div>
        </div>
    </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/swiper.scss";

import "swiper/components/pagination/pagination.min.css";
import "swiper/components/navigation/navigation.min.css";

// import Swiper core and required modules
import SwiperCore, { Autoplay, Pagination, Navigation } from "swiper/core";

// install Swiper modules
SwiperCore.use([Autoplay, Pagination, Navigation]);

import Button from "../SVGs/Button";
export default {
    components: {
        Swiper,
        SwiperSlide,
        carouselbutton: Button,
    },
    data() {
        return {
            images: {
                id1: "./images/pictures/image4.jpg",
                id2: "./images/pictures/image3.jpg",
                id3: "./images/pictures/image5.jpg",
                id4: "./images/pictures/image6.jpg",
                id5: "./images/pictures/image7.jpg",
            },
        };
    },
    methods: {
        goToImg: function (wich) {
            console.log(Swiper);
            // this.swiper.slideTo(i, 200);
        },
    },
};
</script>

<style lang="scss" scoped>
@import "resources/css/sass/allImports";

#swiper_container {

    #swiper_carousel {

        .slides {
            max-height: 70vh;
            height: 50vw;

            .carousel_imgs {
                width: 100%;
                transform: translateY(-6%);
            }
        }
    }
    #carousel_selector {
        display: flex;
        justify-content: space-between;

        margin: 3vw 0 5vw 0;
        padding: 0 35vw 0 35vw;

        height: fit-content;

        .selector_container {
            border-radius: 100%;
            width: 2vw;
            height: 2vw;

            overflow: hidden;

            display: flex;
            justify-content: space-around;
            align-items: center;

            .selector_img {
                border-radius: 100%;
                width: 1.1vw;
                height: 1.1vw;

                border: 0.15vw solid $white;
            }
        }
    }
}
</style>
