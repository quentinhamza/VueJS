<template>
<!-- Nom du label -->
    <label for="rail">Longueur du rail (50-600):</label>

<!-- Type d'input avec les valeurs min et max -->
    <input type="number" id="longueur" name="ral"
        min="0" max="200">

</template>


<script >
export default {
  data () {
    return {
        // Je voulais faire un tableau avec toutes
        // les valeurs comprises enter mon min et mon max 
        // sans avoir besoin de les reporter une par une dans 
        // mon tableau mais je ne sais pas comment faire
        Longueur : [
            0 - 200
        ]
    }
  },
  name: 'Longueur',
  props: {
    type: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
