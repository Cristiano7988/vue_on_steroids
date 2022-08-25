<template>
  <div>
    <Title text="Get the latest tech news!" />
    <section class="featured-posts">
      <PostPreview v-for="post in posts" :post="post" :key="key" />
    </section>
  </div>
</template>

<script>
import posts from '~/data/posts.json';
import PostPreview from '@/components/Posts/PostPreview.vue';

export default {
    data() {
        return {
            posts
        };
    },
    components: { PostPreview }
}
</script>

<style scoped>
.featured-posts {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

@media screen and (max-width: 1080px) {
  .featured-posts {
    display: block;
  }
}
</style>