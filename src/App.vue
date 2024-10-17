<template>
  <div>{{ greet }} {{ name }}</div>
  <br>
  <div v-text="channel" style="font-weight: bold;"></div>
  <br>
  <br>
  <div><b v-text="channel" ></b></div>
  <br>
  <br>
  <h2 v-bind:id="headinId">Attribute Binded</h2>
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
      methods: {
        add(a, b, c) {
          return a + b + c
        },
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
