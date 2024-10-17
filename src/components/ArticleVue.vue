<template>
    <div>
        <h1>Article Component</h1>
        <h2 v-bind="$attrs">Article Title: {{title}}</h2>
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
        },
        inheritAttrs: false,
    }
</script>

<style scoped>

</style>