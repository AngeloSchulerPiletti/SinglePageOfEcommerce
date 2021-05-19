<template>
    <footer>
        <div id="footer_top">
            <hr />
            <LogoPreto id="logopreto" />
            <hr />
        </div>

        <div id="footer_middle">
            <div class="left">
                <h6>CONTATO</h6>
                <div id="order_links">
                    <div><inertia-link>Imprensa</inertia-link></div>
                    <div><inertia-link>Assessoria Privada</inertia-link></div>
                    <div><inertia-link>Elogios</inertia-link></div>
                    <div><inertia-link>Trabalhe Conosco</inertia-link></div>
                    <div><inertia-link>Reclamações</inertia-link></div>
                </div>
            </div>

            <div class="center">
                <h6>NEWSLETTER</h6>
                <div>
                    <form action="getEmail" method="POST">
                        <input type="email" name="" id="" placeholder="Email" />
                        <button type="submit">ENVIAR</button>
                    </form>
                    <hr />
                </div>
            </div>

            <div class="right">
                <h6>REDES SOCIAIS</h6>
                <ul>
                    <li class="media_container">
                        <instagram-icon class="media_icon" /><inertia-link>
                            @begi_forevis</inertia-link
                        >
                    </li>
                    <li class="media_container">
                        <facebook-icon class="media_icon" /><inertia-link
                            >BeGI Style</inertia-link
                        >
                    </li>
                </ul>
            </div>
        </div>

        <div id="footer_bottom">
            <span>@BeGI - Be GI to be Beautiful - CPF 051.057.840-30</span>
        </div>
    </footer>
</template>

<script>
import LogoPreto from "../SVGs/LogoPreto";
import FacebookIcon from "../SVGs/FacebookIcon";
import InstagramIcon from "../SVGs/InstagramIcon";
export default {
    components: {
        LogoPreto,
        FacebookIcon,
        InstagramIcon,
    },
};
</script>

<style lang="scss">
@import "resources/css/sass/allImports";

footer {
    display: flex;
    flex-direction: column;
    align-items: center;

    background-image: linear-gradient(0deg, $notwhite, $redwhite, $redwhite);

    h6,
    span,
    a {
        color: $black;
    }
    h6 {
        @include Font1_SS();
        font-size: 1.8vw;
        margin-bottom: 1vw;
    }
    span {
        @include Font2_SS();
        font-size: 1.1vw;
    }
    a {
        @include Font2_SS();
        font-size: 1.5vw;

        transition-duration: 200ms;
        transition-property: color;

        &:hover{
            color: $notblack;
        }
    }

    #footer_top {
        display: flex;
        width: 100%;

        align-items: center;

        margin-bottom: 5vw;

        #logopreto {
            width: 30vw;
            margin: 0 2vw 0 2vw;
        }
        hr {
            border: none;
            outline: none;

            height: 1px;
            width: 100%;
            background-color: $black;
        }
    }
    #footer_middle {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        margin-bottom: 4vw;

        width: 95%;
        margin: auto;
        justify-items: center;

        .left {
        }
        .center {
            text-align: center;
            
            form {
                display: flex;

                width: 20vw;

                input {
                    border: none;
                    background-color: transparent;
                    font-size: 1vw;

                    flex-grow: 1;

                    transition-duration: 300ms;
                    transition-property: padding;
                    &:focus{
                        padding: 0.3vw;
                    }
                }
                button {
                    background-color: transparent;
                    border: none;
                    font-size: 1.3vw;

                    transition-duration: 300ms;
                    transition-property: color;

                    &:hover{
                        color: $notblack;
                    }
                }
            }
            hr {
                border-color: $black;
                border-width: 1px 0 0 0;
                outline: none;
            }
        }
        .right {
        }

        #order_links {
            display: grid;
            grid-template-rows: 1fr 1fr 1fr;
            grid-template-columns: 1fr 1fr;
        }
        .media_container {
            display: flex;
            align-items: center;

            margin-bottom: 0.5vw;

            .media_icon {
                width: 2vw;
                height: 2vw;

                margin-right: 0.6vw;
            }
        }
    }
    #footer_bottom {
        padding-bottom: 2vw;
        span {
        }
    }
}
</style>
