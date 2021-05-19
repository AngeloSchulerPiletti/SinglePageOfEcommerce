<template>
    <section :class="'secIns_container '+state+'_container'">
        <a :class="state+'_centertop'" href="https://www.instagram.com/mussum_sinceris/"
            ><h4>@begi_forevis</h4></a
        >
        <div :class="'bottom '+state+'_right'">
            <div class="left">
                <inertia-link>
                    <img src="images/pictures/image11.jpg" alt="" />
                    <div style="display: none"><p>Ooooooooooooo</p></div>
                </inertia-link>
            </div>

            <div class="center">
                <inertia-link>
                    <img src="images/pictures/image12.jpg" alt="" />
                    <div style="display: none"><p>Ooooooooo</p></div>
                </inertia-link>
            </div>

            <div class="right">
                <inertia-link>
                    <img src="images/pictures/image13.jpg" alt="" />
                    <div style="display: none"><p>Ooooooooooooo</p></div>
                </inertia-link>
            </div>
        </div>
        <div id="middle_draw" :class="state+'_left'"></div>
    </section>
</template>

<script>
export default {
    props:{
        state: String,
    },
};
</script>

<style lang="scss" scoped>
@import "resources/css/sass/allImports";
@import "resources/css/sass/Components/SectionInstagram/mixins";

.secIns_container {
    display: flex;
    flex-direction: column;
    align-items: center;

    position: relative;

    margin-bottom: 20vw;

    h4 {
        @include Font2_S();
        font-size: 2.5vw;
        margin-bottom: 3vw;
        z-index: 100;
    }
    .bottom {
        z-index: 100;
        display: flex;
        justify-content: center;

        width: 100%;

        .left {
            @include horizontalDivs();
            @include instagramZoom();
        }
        .center {
            @include horizontalDivs();

            margin: 0 4vw 0 4vw;
            transform: translateY(15%);

            transition-property: transform;
            transition-duration: 400ms;

            &:hover {
                transform: scale(1.05) translateY(15%);
            }
        }
        .right {
            @include horizontalDivs();
            @include instagramZoom();
        }
    }
    #middle_draw {
        position: absolute;
        z-index: 0;

        top: 50%;

        background-color: $notblack;
        width: 100%;
        height: 12vw;
    }
}




@include section3_anim();

.none_container{
    opacity: 0;
}
.show_container{
    opacity: 1;
}




.none_centertop{
    opacity: 0;
}
.hide_centertop{
    animation: hiding_centertop 200ms ease-out 0ms 1 normal both;
}
.show_centertop{
    animation: showing_centertop 400ms ease-out 400ms 1 normal both;
}

.none_left{
    opacity: 0;
}
.hide_left{
    animation: hiding_left 200ms ease-out 0ms 1 normal both;
}
.show_left{
    animation: showing_left 450ms ease-out 0ms 1 normal both;
}

.none_right{
    opacity: 0;
}
.hide_right{
    animation: hiding_right 200ms ease-out 0ms 1 normal both;
}
.show_right{
    animation: showing_right 400ms ease-out 400ms 1 normal both;
}


</style>
