<template>
    <div>
        <h1>Put the id to load the user</h1>
        <input type="text" v-model="userId"/>
        <button @click="onLoadUser">Load User</button>
    </div>
</template>

<script>
export default {
    data () {
        return {
            userId: ''
        }
    },
    methods: {
        onLoadUser () {
            this.$router.push(`/users/${this.userId}`)
        }
    }
}
</script>
