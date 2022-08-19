<template>
    <div>
        <Header />
        <section class="posts-page">
            <h1>Posts</h1>
            <ul class="posts-list">
                <li>
                    <nuxt-link to="/posts/1">Do you know what is going on in China?</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/posts/2">What if we dance backwards?</nuxt-link>
                </li>
            </ul>
        </section>
    </div>
</template>

<style scoped>
    .posts-page {
        text-align: center;
    }
    .posts-list {
        list-style: none;
        padding: 0;
        margin: 0;
    }
    .posts-list a {
        text-decoration: none;
        color: darkslategray;
        background: aliceblue;
        display: block;
        padding: 10px;
        margin: 5px;
    }
</style>
<