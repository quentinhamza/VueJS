<template>
    <label v-bind:for="name"> {{label}} </label>
    <textarea v-bind:name="name" v-bind:id="name" cols="30" rows="10"></textarea>
</template>

<script>
export default {
  name: 'TextArea',
  props: {
    name: String,
    label: String,
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
