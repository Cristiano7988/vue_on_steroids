<template>
    <div>
        <p>Hello, admin! Your id is: {{ $route.params.id }}</p>
        <hr />
        <div class="create-post">
            <h2>Create Post</h2>
            <button @click="$router.push('/admin/new-post')" >Create Post</button>
        </div>
        <hr />
        <div class="post-list">
            <h2>List of Posts</h2>
            <PostList />
        </div>
    </div>
</template>

<script>
import PostList from '~/components/Posts/PostList.vue';
export default {
    validate(data) {
        return /^\d+$/.test(data.params.id);
    },
    components: { PostList }
}
</script>

<style>
h2 {
    font-family: 'Aboreto';
}

.post-list, .create-post {
    padding-top: 20px;
    padding-bottom: 40px;
}
</style>