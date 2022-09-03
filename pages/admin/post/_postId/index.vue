<template>
    <div class="admmin-post-page">
        <section class="update-form">
            <h2>Edit Post</h2>
            <AdminPostForm :post="loadedPost" />
        </section>
    </div>
</template>

<script>
    import AdminPostForm from '~/components/Admin/AdminPostForm';
    import posts from '@/data/posts.json';

    export default {
        data() {
            return {
                loadedPost: posts[this.$route.params.postId - 1]
            }
        },
        components: {
            AdminPostForm
        }
    }
</script>