<template>
    <layout>
        <main>
            <Carousel :state="anim_cmd.sec_car" id="section_carousel" />
            <Sec1 :state="anim_cmd.sec_1" id="section_1" />
            <Sec2 :state="anim_cmd.sec_2" id="section_2" />
            <SecIns :state="anim_cmd.sec_3" id="section_3" />
        </main>
    </layout>
</template>

<script>
import App from "./Layouts/App";

import Carousel from "./Components/Carousel";
import Section1 from "./Components/Section1";
import Section2 from "./Components/Section2";
import SectionInstagram from "./Components/SectionInstagram";
export default {
    data() {
        return {
            anim_cmd:{
                sec_car: "none",
                sec_1: "none",
                sec_2: "none",
                sec_3: "none",
            },
        };
    },
    created() {
        window.addEventListener("scroll", this.handleScroll);
    },
    destroyed() {
        window.removeEventListener("scroll", this.handleScroll);
    },
    components: {
        layout: App,
        Carousel,
        Sec1: Section1,
        Sec2: Section2,
        SecIns: SectionInstagram,
    },
    methods: {
        handleScroll(event) {
            var el0 = document.querySelector("#section_carousel"),
                el1 = document.querySelector("#section_1"),
                el2 = document.querySelector("#section_2"),
                el3 = document.querySelector("#section_3");

            var el0Coo = el0.getBoundingClientRect(),
                el1Coo = el1.getBoundingClientRect(),
                el2Coo = el2.getBoundingClientRect(),
                el3Coo = el3.getBoundingClientRect();

            var scrollDelta = document.documentElement.scrollHeight,
                scrollY = document.documentElement.scrollTop,
                windowHeight = window.innerHeight;

            var margin = (2*windowHeight)/7;

            console.log("window height: "+windowHeight);
            console.log("elementY: "+el1Coo.y + margin);

            //Active Section1
            if(el1Coo.y + margin <= windowHeight){
                this.$data.anim_cmd.sec_1 = "show";
            }
            // if(el1Coo.y + margin > windowHeight && this.$data.anim_cmd.sec_1 == "show"){
            //     this.$data.anim_cmd.sec_1 = "hide";
            // }



            //Active Section2
            if(el2Coo.y + margin <= windowHeight){
                this.$data.anim_cmd.sec_2 = "show";
            }
            if(el2Coo.y + margin > windowHeight && this.$data.anim_cmd.sec_2 == "show"){
                this.$data.anim_cmd.sec_2 = "hide";
            }


            //Active Section3
            if(el3Coo.y + margin <= windowHeight){
                this.$data.anim_cmd.sec_3 = "show";
            }
            if(el3Coo.y + margin > windowHeight && this.$data.anim_cmd.sec_3 == "show"){
                this.$data.anim_cmd.sec_3 = "hide";
            }

        },
    },
};
</script>

<style lang="scss">
@import "resources/css/sass/allImports";

main {
    background-color: $redwhite;
}
</style>
