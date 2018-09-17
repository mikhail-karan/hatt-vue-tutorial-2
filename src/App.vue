<template>
  <div id="app">
    <!-- <square text="This is a square" size="small"/>
    <square text="This is a square" size="medium"/>
    <square text="This is a square" size="large"/>
    <square text="This is a square" size="large" color="#000"/> -->
    <square
      v-for="data in myJson"
      v-bind:key="data.text"
      v-bind:text="data.text"
      v-bind:size="data.size"
      v-bind:color="data.color"
    />
  </div>
</template>

<script>
import square from './components/square.vue'
import json from './json/data.json'

export default {
  name: 'app',
  data(){
    return{
      myJson: json
    }
  },
  components: {
    square
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
