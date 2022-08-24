<template>
  <div>
    <Header />
    <section class="container">
      <h1>Get the latest tech news!</h1>
    </section>
    <section class="featured-posts">
      <nuxt-link v-for="(post, key) in posts" :key="key" :to="post.to">
        <article class="post-preview">
          <div class="post-thumbnail">
            <img :src="post.thumbnail" />
          </div>
          <div class="post-content">
            <h1>{{ post.title }}</h1>
            <p>{{ post.text }}</p>
          </div>
        </article>
      </nuxt-link>
    </section>
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
export default {
    data() {
      return {
        posts: [
          {
            thumbnail: 'https://s.yimg.com/ny/api/res/1.2/4.YiYj1m4s6pMrIU8HpYYQ--/YXBwaWQ9aGlnaGxhbmRlcjt3PTk2MDtoPTYzODtjZj13ZWJw/https://s.yimg.com/os/creatr-uploaded-images/2022-02/3f209330-8db1-11ec-afd9-1652014d9db4',
            title: 'Page Title 1',
            text: 'Preview Text 1',
            to: `/posts/${1}`
          },
          {
            thumbnail: 'https://cdn.falauniversidades.com.br/wp-content/uploads/2020/09/02132947/danca-1.jpg',
            title: 'Page Title 2',
            text: 'Preview Text 2',
            to: `/posts/${1}`
          },
        ]
      }
    },
    components: { Header }
}
</script>

<style scoped>
.container {
  font-family: 'Aboreto';
}

.featured-posts {
  display: flex;
}

@media screen and (max-width: 1080px) {
  .featured-posts {
    display: block;
  }
}

@media screen {
  
}

.post-preview {
  height: 300px;
  position: relative;
  overflow: hidden;
  padding: 10px 0;
  margin: 40px 0;
}

.post-thumbnail img {
  width: 100%;
  position: relative;
  left: 0%;
}

.post-content {
  position: absolute;
  background-color: rgba(999, 999, 999, .4);
  width: 100%;
  bottom: 0;
  padding: 0 80px;
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

.post-content h1 {
  font-family: 'Aboreto';
  font-weight: bolder;
}

.post-content p {
  font-family: fantasy;
}
</style>