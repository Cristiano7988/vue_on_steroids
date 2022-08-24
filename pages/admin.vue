<template>
    <div>
        <Title text="Admin Section" />
        <section class="admin-page">
            <input type="text" v-model="adminId"/>
            <button @click="onLoadAdmin">Load Admin</button>
            <nuxt-child />
        </section>
    </div>
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