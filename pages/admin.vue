<template>
    <section>
        <h1>Admin Section</h1>
        <input type="text" v-model="adminId"/>
        <button @click="onLoadAdmin">Load Admin</button>
        <nuxt-child />
    </section>
</template>

<script>
export default {
    data () {
        return {
            adminId: ''
        }
    },
    methods: {
        onLoadAdmin () {
            this.$router.push(`/admin/${this.adminId}`)
        }
    },
    layout: 'admin'
}
</script>