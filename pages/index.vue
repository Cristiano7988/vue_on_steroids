<template>
  <div>
    <Header />
    <section class="container">
      <h1>Welcome to the main page!</h1>
      <nuxt-link to="/users">users</nuxt-link>
    </section>
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
export default {
    components: { Header }
}
</script>
