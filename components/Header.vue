<template>
    <header class="header">
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

<style scoped>
    .header {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        background:darkslategray;
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
    }
</style>