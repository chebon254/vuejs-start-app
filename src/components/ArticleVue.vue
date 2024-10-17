<template>
    <div>
        <h1>Article</h1>
        <h2>Article Title: {{title}}</h2>
        <h2>Likes {{likes}}</h2>
        <h2>Published: {{ isPublished ? "Yes" : "No" }}</h2>
    </div>
</template>

<script>
    export default {
        name: "ArticleVue",
        props: {
            title: {
                type: String,
                required: true,
                default: "Default Article Title"
            }, 
            likes: Number,
            isPublished: Boolean
        }
    }
</script>

<style scoped>

</style>