<template>
  <div>
    <div class="main-title">
      <Title text="Get the latest tech news!" />
    </div>
    <section class="featured-posts">
      <PostPreview v-for="(post, key) in posts" :post="post" :key="key" />
    </section>
  </div>
</template>

<script>
import posts from '~/data/posts.json';
import PostPreview from '@/components/Posts/PostPreview';

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
.main-title {
  background-image: url('~assets/img/paisagem.jpg');
  color: white;
  background-repeat: no-repeat;
  background-size: cover;
  padding: 80px;
  animation: auto-scroll 80s infinite;
}

@keyframes auto-scroll
{
  0% {background-position: 0% 0%; }
  50% {background-position: 0% 100%; }
  100% {background-position: 0% 0%; }
  
}

.main-title h1 {
  margin: 0;
  text-shadow: 2px 2px 5px black;
}

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