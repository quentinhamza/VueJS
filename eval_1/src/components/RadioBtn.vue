<template>
  <span>{{heure}}</span>
  <span v-for="option in options" :key="option">
    <input type="radio" id="option.idRadio" name="heure">
    <label v-bind:for="option.idRadio">{{option.heure}}</label>
  </span>
</template>

<script>
export default {
  name: 'RadioBtn',
  props: {
    heure: String,
    idRadio: String,

  },
  data(){   
  return {  
    options: [ 
      {
        heure: '12h',
      }, 
      {
        heure: '12h30',
      },
      {
        heure: '13h',
      },
      {
        heure: '13h',
      },
      {
        heure: '13h30',
      },
      {
        heure: '14h',
      },
      {
        heure: '14h30',
      },
      {
        heure: '15h',
      },
      {
        heure: '15h30',
      },
      {
        heure: '16h',
      },
      {
        heure: '16h30',
      },
      {
        heure: '17h',
      },
      {
        heure: '17h30',
      },
      {
        heure: '18h',
      },
      {
        heure: '18h30',
      },
      {
        heure: '19h',
      },
      {
        heure: '19h30',
      },
    ]
    
  }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
input{
  padding: 10px
}
</style>