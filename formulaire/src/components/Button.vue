<template>
  <button v-on:click="$emit('validation')">valider</button>
</template>
 
<script>
export default {
  name: "Button",
  props: {
    msg: String,
  },
  data(){
    return {
    
  }
}
};
</script>
 
<style>
</style>