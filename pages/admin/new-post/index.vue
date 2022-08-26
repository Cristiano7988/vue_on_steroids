<template>
    <div class="admin-new-post-page">
        <section class="new-post-form">
            <h2>Create Post</h2>
            <form @submit.prevent="onSave">
                <FormField v-model="editedPost.author">Author</FormField>
                <FormField v-model="editedPost.title">Title</FormField>
                <FormField v-model="editedPost.thumbnail">Thumbnail</FormField>
                <FormField v-model="editedPost.texts" type="textarea">Texts</FormField>
                <div class="buttons-container">
                    <FormButton type="submit">Create Post</FormButton>
                    <FormButton type="button" @click="onCancel" btnClass="cancel">Cancel</FormButton>
                </div>
            </form>
        </section>
    </div>
</template>

<script>
    import FormField from '~/components/UI/FormField';
    import FormButton from '~/components/UI/FormButton';

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
            FormField,
            FormButton
        },
        methods: {
            onSave() {
                console.log(this.editedPost)
            },
            onCancel() {
                this.$router.push('/admin')
            }
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