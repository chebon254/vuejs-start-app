<template>
<br>
  <br>
  <br>
  <div>
    <!-- <pre>
      {{JSON.stringify(formValues, null, 2)}}
    </pre> -->
  </div>
  <!-- <form @submit="submitForm">
    <div>
      <label for="name">Name</label>
      <input type="text" id="inputname" v-model="formValues.name">
    </div>
    <div>
      <input type="checkbox" name="checkbox" v-model="formValues.remoteWork">
      <label for="checkbox">Are you open to remote work?</label>
    </div>
    <div>
      <input type="checkbox" name="html" value="html" id="inputcss" v-model="formValues.skillSet">
      <label for="html">HTML</label>
      <input type="checkbox" name="css" value="css" id="inputcss" v-model="formValues.skillSet">
      <label for="css">CSS</label>
      <input type="checkbox" name="js" value="js" id="inputjs" v-model="formValues.skillSet">
      <label for="js">JAVASCRIPT</label>
    </div>
    <div>
      <input type="radio" name="0-3" value="0-3" id="input0-3" v-model="formValues.yearsofExperience">
      <label for="0-3">0-3</label>
      <input type="radio" name="4-6" value="4-6" id="input4-6" v-model="formValues.yearsofExperience">
      <label for="4-6">4-6</label>
      <input type="radio" name="6-9" value="6-9" id="input6-9"  v-model="formValues.yearsofExperience">
      <label for="6-9">6-9</label>
    </div>
    <div>
      <button>Submit</button>
    </div>
  </form> -->
  <br>
  <br>
  <div>{{ greet }} {{ name }}</div>
  <br>
  <div v-text="channel" style="font-weight: bold;"></div>
  <br>
  <br>
  <div><b v-text="channel" ></b></div>
  <br>
  <br>
  <h2 v-bind:id="inputheadinId">Attribute Binded</h2>
  <br>
  <br>
  <button v-bind:disabled="isDisabled">Bind Diasable Attribute</button>
  <br>
  <br>
  <br>
  <br>
  <h1 v-if="num === 0">Number is Zero</h1>
  <h1 v-else>Number is not Zero</h1>
  <br>
  <br>
    <br>
    <template v-if="display">
      <h2>Chebon</h2>
      <h2>Kelvin</h2>
      <h2>Kibet</h2>
    </template>
    <br>
  <br>
  <br>
  <br>
  <h2 v-for="(name, index) in listNames" v-bind:key="name">{{index}} {{ name }}</h2>
  <br>
  <h2 v-for="(name, key, index) in arrayNames" v-bind:key="name">{{index}} {{key}} {{name.first}} {{name.last}}</h2>
  <br>
  <br>
  <br>

  <br>
  <br>
      <h2>{{eventName}}</h2>
      <div>
        <button v-if="eventName === 'Event Name: Kibet'" v-on:click="eventName = 'New Event Name: Kelvin'">Change Name</button>
        <button v-else v-on:click="eventName = 'Event Name: Kibet'">Change Name</button>
      </div>
  <br>
  <br>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
    formValues: {
      name: "",
      remoteWork: false,
      skillSet: [],
      // yearsofExperience: []
    },
      methods: {
        add(a, b, c) {
          return a + b + c
        },
        // submitForm(event) {
        //   event.preventDefault();
        //   console.log("Form Values" + this.formValues)
        // }
      },
      eventName: "Event Name: Kibet",
      name: "Chebon kelvin Kibet",
      listNames: ["Kelvin", "Ben", "Manuel", "Kelly"],
      arrayNames: [
        {first: "Kelvin", last: "Chebon"},
        {first: "Ben", last: "Chebon"},
        {first: "Manuel", last: "Chebon"},
        {first: "Kelly", last: "Chebon"},
      ],
      arrayList: {

      },
      greet: "Hello, ",
      channel: "Cretivdev & Affiliate pro",
      headinId: "heading",
      isDisabled: false, 
      num: 0,
      display: true,
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
