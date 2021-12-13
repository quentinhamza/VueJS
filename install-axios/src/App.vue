<template>
  <APIBTC/>
  <APIGitHub/>
</template>

<script>
import APIGitHub from './components/APIGitHub';
import APIBTC from './components/APIBTC';
export default {
  name: 'App',
  components: {
    APIGitHub,
    APIBTC,
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
