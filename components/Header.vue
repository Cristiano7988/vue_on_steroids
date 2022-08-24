<template>
    <header :class="['header', classes]">
        <ul class="nav-items">
            <li>
                <nuxt-link to="/">Home</nuxt-link>
            </li>
            <li>
                <nuxt-link to="/admin">Admin</nuxt-link>
            </li>
            <li>
                <nuxt-link to="/about">About Us</nuxt-link>
            </li>
            <li>
                <nuxt-link to="/posts">Posts</nuxt-link>
            </li>
        </ul>
    </header>
</template>

<script>
export default {
    props: {
        classes: {
            type: String,
            default: ''
        }
    }
}
</script>

<style scoped>
    .background-primary {
        background:darkslategray;
    }
    .background-secondary {
        background:chocolate;
    }
    .header {
        font-family: Aboreto;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        color: white;
    }
    .nav-items {
        list-style: none;
        padding: 0px;
        margin: 0;
        display: flex;
        width: 100%;
        justify-content: space-around;
    }
    .nav-items a {
        display: block;
        padding: 20px;
        color: white;
        text-decoration: none;
        transition: background 1s;
    }
    .background-primary .nav-items a:hover {
        background: lightseagreen;
    }
    .background-secondary .nav-items a:hover {
        background: sandybrown;
    }
</style>