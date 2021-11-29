<template>
    <label v-bind:for="name">{{label}}</label>
    <select v-bind:name="name" v-bind:id="name">

      <option v-for="options in  options" v-bind:key="name.character" v-bind:value"option.value">{{option.select}}</option>
    </select>
</template>

<script>
export default {
  data () {
    return {
      list : [{
        value : "etudiant",
        text : "Étudiant",
      }, {
        value : "profesionnel",
        text : "Professionnel",
      }
      ]
    }
  },
  name: 'Select',
  props: {
    name: String,
    label: String,
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
