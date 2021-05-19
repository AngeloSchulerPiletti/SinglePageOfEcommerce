<template>
    <footer>
        <div id="footer_top">
            <hr />
            <LogoPreto id="logopreto"/>
            <hr />
        </div>

        <div id="footer_middle">
            <div>
                <h6>CONTATO</h6>
                <ul>
                    <li><inertia-link>Trabalhe Conosco</inertia-link></li>
                    <li><inertia-link>Assessoria Privada</inertia-link></li>
                    <li><inertia-link>Elogios</inertia-link></li>
                    <li><inertia-link>Reclamações</inertia-link></li>
                    <li><inertia-link>Imprensa</inertia-link></li>
                </ul>
            </div>

            <div>
                <h6>NEWSLETTER</h6>
                <div>
                    <form action="getEmail" method="POST">
                        <input type="email" name="" id="" placeholder="Email" />
                        <button type="submit">ENVIAR</button>
                    </form>
                    <hr />
                </div>
            </div>

            <div>
                <h6>SOBRE NÓS</h6>
                <ul>
                    <li>
                        <inertia-link
                            ><img src="" alt="" />História</inertia-link
                        >
                    </li>
                    <li>
                        <inertia-link
                            ><img src="" alt="" />BeGI Green</inertia-link
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
export default {
    components: {
        LogoPreto,
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

    #footer_top {
        display: flex;
        width: 100%;

        align-items: center;

        margin-bottom: 8vw;

        #logopreto{
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
        display: flex;
        justify-content: space-around;
        margin: 1vw 0 1vw 0;

        width: 100%;

        h6 {
            color: $black;
        }
        a {
            color: $black;
        }
    }
    #footer_bottom {
        padding-bottom: 2vw;
        span {
            color: $black;
        }
    }
}
</style>
