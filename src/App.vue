<template>
  <div>
    <!-- <GreetVue name="Kelvin" heroName="KK"/>
    <GreetVue name="Kibet" heroName="KC"/> -->
    
    <!-- <ArticleVue id="myArticle" :likes="50" :isPublished="false"/> -->
    <!-- <h3>AppComponent username: {{name}}</h3>
    <ComponentCVue /> -->
    <!-- <button @click="showPopup = true">Show Popup</button>
    <PopupVue v-show="showPopup" @close="closePopup"/>  -->
    <!-- <input type="text" v-model="name">
    <InputVue/> -->
    <!-- <CardVue content="Card Content 1"/> -->
    <!-- <CardVue></CardVue>
    <CardVue>Card Content</CardVue>

    <CardVue>
      <h2>Card content</h2>
    </CardVue>
    <CardVue>
      <img src="https://picsum.photos/200"/>
    </CardVue>

    <CardVue>
      <template v-slot:header>
        <h3>Header</h3>
      </template>
      <template v-slot:default>
        <h3>Content</h3>
        <img src="https://picsum.photos/200"/>
      </template>
      <template v-slot:footer>
        <h3>Footer</h3>
        <button>Veiw Details</button>
      </template>
    </CardVue> -->

    <NameListVue>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName}} {{ slotProps.lastName}}
      </template>
    </NameListVue>

    <NameListVue>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName}} {{ slotProps.lastName}}
      </template>
    </NameListVue>

    <NameListVue>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName}} {{ slotProps.lastName}}
      </template>
    </NameListVue>
  </div>
</template>

<script>
import NameListVue from './components/NameListVue.vue'

// import CardVue from './components/CardVue.vue'
// import InputVue from './components/InputVue.vue'
// import PopupVue from './components/PopupVue.vue'
// import ComponentCVue from './components/ComponentC.vue'
// import ArticleVue from './components/ArticleVue.vue'
// import GreetVue from './components/GreetVue.vue'

export default {
  name: 'App',
  components : {
    NameListVue,
    // CardVue,
    // InputVue,
    // PopupVue,
    // GreetVue,
    // ArticleVue,
    // ComponentCVue,
  },
  // Props 2
  // data() {
  //   return {
  //     showPopup: false
  //   }
  // },
  // methods: {
  //   closePopup(name){
  //     this.showPopup = false
  //     console.log('name', name)
  //   }
  // }
  //Props 1
  // data(){
  //   return{
  //     name: "Cartoon"
  //   }
  // },
  // provide() {
  //   return {
  //     username: this.name
  //   }
  // }
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
