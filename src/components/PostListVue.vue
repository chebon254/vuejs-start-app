<template>
    <div>
        <button @click="getPosts">Load Posts</button>
        <h4>{{errorMessage}}</h4>
        <div v-for="post in posts" :key="post.id">
            <h3>{{post.id}} {{post.title}}</h3>
            <p>{{post.body}}</p>
            <hr>
            <br>
        </div>

    </div>
</template>

<script>
import axios from 'axios'
    export default {
        name: "PostListVue",
        data() {
            return{
                posts: [],
                errorMessage: ""
            }
        },
        methods: {
            getPosts() {
                axios.get('https://jsonplaceholder.typicode.com/posts')
                .then((response)=>{
                    console.log(response.data)
                    this.posts = response.data
                })
                .catch((error)=>{
                    console.log(error)
                    this.errorMessage = "Error Fetching Data"
                })
            }
        }
    }
</script>

<style scoped>

</style>