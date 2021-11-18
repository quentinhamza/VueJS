<template>

  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>

  <ul v-if="seen">
        <li v-for="item in message" :key="item.message"> {{ item }} </li>
  </ul>  
  
  <button v-on:click="seen = !seen"> CLICK </button>

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
        message: ['Mathis','Pierre','Romain','Souri','Quentin'],
        seen: true,
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
</style>
