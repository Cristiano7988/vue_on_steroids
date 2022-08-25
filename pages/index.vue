<template>
  <div>
    <Title text="Get the latest tech news!" />
    <section class="featured-posts">
      <nuxt-link v-for="({texts, title, id, thumbnail}, key) in posts" :key="key" :to="'/posts/'+id">
        <article class="post-preview">
          <div class="post-thumbnail">
            <img :src="thumbnail" />
          </div>
          <div class="post-content">
            <h1>{{ title }}</h1>
            <p>{{ texts[0].split('.')[0] }}.</p>
          </div>
        </article>
      </nuxt-link>
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
.featured-posts {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

@media screen and (max-width: 1080px) {
  .featured-posts {
    display: block;
  }
}

.post-preview {
  height: 300px;
  position: relative;
  overflow: hidden;
  padding: 10px 0;
  margin: 40px 0;
}

.post-thumbnail img {
  position: relative;
  left: 0%;
}

.post-content {
  position: absolute;
  background-color: rgba(999, 999, 999, .6);
  width: 100%;
  bottom: 0;
  margin: 40px 0;
  color: darkslategrey;
  box-shadow: 0px 0px 0px black;
  text-shadow: 0px 0px 0px black;
}

.post-preview:hover img {
  width: 110%;
  left: -10%;
  transition: width 6s, left 6s;
}

.post-preview:hover .post-content {
  box-shadow: 1px 1px 35px black;
  text-shadow: 1px 1px 10px black;
  transition: box-shadow 1s, text-shadow .2s;
}

.post-content p {
  font-family: fantasy;
}
</style>