<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>

  <ul>
    <li v-for="item in message" :key="item.message" id="tableau">{{ item }}</li>
    </ul>

    <button v-on:click="Afficher">CLICK</button>
  
  </template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {    
      return {
       message: ['Mathis','Pierre','Romain','Souri','Quentin']
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

#tableau{
  display: none;
}
</style>
