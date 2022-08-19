<template>
    <div class="container">
        <Header />
        <nuxt />
    </div>
</template>

<script>
import Header from "~/components/Header.vue";

export default {
    components: {
        Header
    }
}
</script>

<style>
.container {
    text-align: center
}
</style>