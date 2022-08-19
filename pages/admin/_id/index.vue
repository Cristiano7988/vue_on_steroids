<template>
    <p>Hello, admin! Your id is: {{ $route.params.id }}</p>
</template>

<script>
export default {
    validate (data) {
        return /^\d+$/.test(data.params.id)
    }
}
</script>