<template>
  <!-- <GreetVue name="Kelvin" heroName="KK"/>
  <GreetVue name="Kibet" heroName="KC"/> -->
  
  <ArticleVue :likes="50" :isPublished="false"/>
</template>

<script>
import ArticleVue from './components/ArticleVue.vue'
// import GreetVue from './components/GreetVue.vue'

export default {
  name: 'App',
  components : {
    // GreetVue,
    ArticleVue,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
button{
  padding: 10px 20px;
  border-radius: 10px;
}
</style>
