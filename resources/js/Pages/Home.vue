<template>
    <layout>
        <main>
            <Carousel/>
            <Sec1/>
            <Sec2/>
            <SecIns/>
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
    components: {
        layout: App,
        Carousel,
        Sec1: Section1,
        Sec2: Section2,
        SecIns: SectionInstagram,
    },
};
</script>

<style lang="scss">
@import 'resources/css/sass/allImports';

main{
    background-color: $redwhite;
}

</style>
