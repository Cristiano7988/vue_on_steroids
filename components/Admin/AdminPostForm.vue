<template>
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
</template>

<script>
import FormField from '~/components/UI/FormField';
import FormButton from '~/components/UI/FormButton';

export default {
    data() {
        if(this.post) this.post.texts = this.post.texts.join("\n\n")
        
        return {
            editedPost: this.post ? { ...this.post } : {
                author: '',
                title: '',
                content: '',
                thumbnail: ''
            }
        }
    },
    props: {
        post: {
            type: Object,
            required: false
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
    },
    mounted() {

    }
}
</script>