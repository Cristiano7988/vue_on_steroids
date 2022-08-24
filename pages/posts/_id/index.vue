<template>
    <div>
        <Title :text="title" />
        <section class="single-post-page">
            <img :src="thumbnail" />
            <span>Written by {{ author }}</span><br />
            <span>Published in {{ created_at }}</span>
            <hr />
            <p v-for="(text, index) in texts" :key="index">{{ text }}</p>
            <hr />
        </section>
    </div>
</template>

<script>
import posts from '~/data/posts.json';

export default {
    data () {
        return {
            ...posts[this.$route.params.id - 1]
        }
    }
}
</script>