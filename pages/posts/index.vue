<template>
    <div>
        <Title text="Posts" />
        <section class="posts-page">
            <ul class="posts-list">
                <li v-for="(post, index) in posts" :key="index">
                    <nuxt-link :to="'/posts/'+post.id">{{ post.title }}</nuxt-link>
                </li>
            </ul>
        </section>
    </div>
</template>

<script>
import posts from '~/data/posts.json';

export default {
    data() {
        return {
            posts
        }
    }
}
</script>

<style scoped>
    .posts-list a {
        color: darkslategray;
        background: aliceblue;
        display: block;
        padding: 10px;
        margin: 5px;
        font-family: system-ui;
    }
</style>
<