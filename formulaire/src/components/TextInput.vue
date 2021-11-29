<template>
    <label v-bind:for="name"> {{label}} </label>
    <input type="text" v-bind:name="name">
</template>

<script>
export default {
  name: 'TextInput',
  props: {
    name: String,
    label: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
