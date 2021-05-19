<template>
    <section id="secIns_container">
        <a href="https://www.instagram.com/mussum_sinceris/"
            ><h4>@begi_forevis</h4></a
        >
        <div class="bottom">
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
        <div id="middle_draw"></div>
    </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "resources/css/sass/allImports";
@import "resources/css/sass/Components/SectionInstagram/mixins";

#secIns_container {
    display: flex;
    flex-direction: column;
    align-items: center;

    position: relative;

    margin-bottom: 14vw;

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

        padding: 0 10vw 0 10vw;

        .left {
            @include horizontalDivs();
        }
        .center {
            @include horizontalDivs();
            
            margin: 0 4vw 0 4vw;
            transform: translateY(15%);
        }
        .right {
            @include horizontalDivs();
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
</style>
