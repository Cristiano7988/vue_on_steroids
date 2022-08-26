<template>
    <div>
        <Title text="Posts" />
        <section class="posts-page">
            <PostList />
        </section>
    </div>
</template>
<script>
import PostList from "~/components/Posts/PostList.vue";

export default {
    components: {
        PostList
    }
}
</script>