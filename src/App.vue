<template>
  <div>
    <!-- <GreetVue name="Kelvin" heroName="KK"/>
  <GreetVue name="Kibet" heroName="KC"/> -->
  
  <!-- <ArticleVue id="myArticle" :likes="50" :isPublished="false"/> -->
  <h3>AppComponent username: {{name}}</h3>
  <ComponentCVue />
  </div>
</template>

<script>
import ComponentCVue from './components/ComponentC.vue'
// import ArticleVue from './components/ArticleVue.vue'
// import GreetVue from './components/GreetVue.vue'

export default {
  name: 'App',
  components : {
    // GreetVue,
    // ArticleVue,
    ComponentCVue,
  },
  data(){
    return{
      name: "Cartoon"
    }
  },
  provide() {
    return {
      username: this.name
    }
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
