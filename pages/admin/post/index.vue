<template>
    <div class="admin-new-post-page">
        <section class="new-post-form">
            <h2>Create Post</h2>
            <AdminPostForm />
        </section>
    </div>
</template>

<script>
import AdminPostForm from '~/components/Admin/AdminPostForm.vue';

    export default {
        data() {
            return {
                editedPost: {
                    author: '',
                    title: '',
                    thumbnail: '',
                    texts: ''
                }
            }
        },
        components: {
            AdminPostForm
        }
    }
</script>

<style>
.admin-new-post-page {
    padding-top: 20px;
}
h2 {
    font-family: 'Aboreto';
}
.new-post-form {
    max-width: 300px;
    margin: auto;
}

.buttons-container {
    display: flex;
    justify-content: center;
}
</style>