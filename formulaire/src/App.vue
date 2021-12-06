<template>
  <div>
    <h1 :style="{color:colorie}">Coucou</h1>
  </div>
  <Title title="Formulaire de Contact"/>
    <div v-if="step === 'step 1'">
      <div>
        <TextInput name="name" label="Prénom"/>
        <TextInput name="lastname" label="Nom"/>
      </div>
      <div>
        <DateInput name="birthday" label="Date de Naissance"/>
      </div>
      <button  v-on:click="step = 'step 2'"> Next step</button>

    </div>
      <div v-if="step === 'step 2'">
        <TextArea :name="message" label="Message"/>
        <button  v-on:click="step = 'step 3'"> Next step</button>
      </div>
      <div v-if="step === 'step 3'">
        <Select :name="Sexe"/>
        {{select}}
      </div>
      <div>
        <Button msg="" v-on:validation="colorie='green'"/>
      </div>
      <div>
        <!--
        <BtnForm type="submit" text="Envoyer"/>
        <BtnForm type="reset" text="Réinitialiser"/>
        -->
      </div>
   

</template>

<script>
import Title from './components/Title.vue';
import TextInput from './components/TextInput.vue';
import DateInput from './components/DateInput.vue';
import TextArea from './components/TextArea.vue';
import Select from './components/Select.vue';
import Button from './components/Button.vue';

export default {
  data () {
    return {
      step : 'step 1',
      colorie:'red',
    }
  },
  name: 'App',
  components: {
    Title,
    TextInput,
    DateInput,
    TextArea,
    Select,
    Button,
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
template{
  display: flex;
  flex-direction: row;
}
div{
  margin-top: 10px;
}
</style>
