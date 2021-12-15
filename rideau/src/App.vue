<template>
<!-- juste pour aligner les éléments horizontalement -->
<div style="display: flex">
  <div>
    <h1>Tringle Rail</h1> 
    <img id="img-rail" src="./assets/tringles-rail.jpg">
  </div>
  <div>
    <div>
      <h2>Personnalisez votre produit</h2>
    </div>
    <!-- Step pour faire un système d'étape et griser
    la seconde partie de la personnalisation -->
    <div v-if="step === 'step 1'">
      <Longueur name="rail" label="Longueur du rail"/>
    </div>
    <div>
    <!-- go étape 2 -->
      <button  v-on:click="step = 'step 2'"> Valider</button>
    </div>
    <div v-if="step === 'step 2'">
    
    </div>
    <div>
    <!-- go étape 3 -->
    <button  v-on:click="step = 'step 3'"> Valider</button>
    </div>
    <div v-if="step === 'step 3'">
    
  </div>

  </div>
</div>
  
</template>

<script>
import Longueur from "./components/Longueur"
export default {
  name: 'App',
  components: {
    Longueur,


  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
#img-rail {
  width: 500px;
}
</style>
