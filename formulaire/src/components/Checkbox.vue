<template>
    <label for="{{name}}"> {{label}} </label>
    <textarea name="{{name}}" id="{{name}}" cols="30" rows="10"></textarea>
</template>

<script>
export default {
  name: 'Title',
  props: {
    name: String,
    label: String,
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
