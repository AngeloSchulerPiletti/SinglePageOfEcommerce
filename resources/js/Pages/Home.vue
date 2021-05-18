<template>
    <layout>
        <main>
            <h1>Este é o main</h1>
        </main>
    </layout>
</template>

<script>
import App from "./Layouts/App";
export default {
    components: {
        layout: App,
    },
};
</script>

<style lang="scss">
h1{
    color: red;
}
</style>
