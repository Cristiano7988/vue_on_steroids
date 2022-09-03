<template>
    <ul class="posts-list">
        <li v-for="(post, index) in posts" :key="index">
            <PostPreview
                :is-admin="isAdmin"
                :post="post"
                :preview="false"
            >
                {{ post.title }}
            </PostPreview>
        </li>
    </ul>
</template>

<script>
import posts from '~/data/posts.json';
import PostPreview from './PostPreview.vue';

export default {
    data() {
        return {
            posts
        };
    },
    props: {
        isAdmin: {
            type: Boolean,
            default: false
        }
    },
    components: { PostPreview }
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
    .posts-list a:hover {
        background: chocolate;
        color: white;
        letter-spacing: 5px;
        transition: background 1s, color .1s, letter-spacing 10s;
    }
</style>