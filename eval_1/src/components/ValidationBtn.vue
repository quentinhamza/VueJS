<template>
 <input v-on:click="$emit('validation'), $emit('step')" v-bind:type="type" value="Save and continue" />
</template>

<script>
export default {
  name: 'ValidationBtn',
  props: {
    text: String,
    type: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>