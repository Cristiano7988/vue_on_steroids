<template>
    <h1>{{ text }}</h1>
</template>

<script>
export default {
    props: {
        text: {
            type: String,
            default: ''
        }
    }
}
</script>

<style scoped>
h1 {
    text-align: center;
    font-family: 'Aboreto';
}
</style>