<template>
    <nav>
        <div>
            <inertia-link><img src="" alt="" /></inertia-link>
        </div>
        <div>
            <ul id="menu_links">
                <li><inertia-link>ROUPAS</inertia-link></li>
                <li><inertia-link>ACESSÓRIOS</inertia-link></li>
                <li><inertia-link>JOIAS</inertia-link></li>
                <li><inertia-link>CONTATO</inertia-link></li>
                <li><inertia-link>SOBRE NÓS</inertia-link></li>
            </ul>
        </div>
        <div>
            <inertia-link><img src="" alt="" /></inertia-link>
            <inertia-link><img src="" alt="" /></inertia-link>
            <inertia-link><img src="" alt="" /></inertia-link>
        </div>
    </nav>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import 'resources/css/sass/allImports';

nav{
  display: flex;
  justify-content: space-between;
  padding: 0.5vw;

  background-color: $black;

  transition-property: padding;
  transition-duration: 200ms;

  &:hover{
    padding: 1vw;
  }

  #menu_links{
    li{
      display: inline-block;
      margin: 0 1.2vw 0 1.2vw;
      
      a{
        @include Font2_SS();
        color: $white;
        font-size: 1.2vw;

        transition-property: color;
        transition-duration: 300ms;

        &:hover{
          color: $redwhite;
        }
      }
    }
  }
}
</style>
