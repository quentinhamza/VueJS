<template>
  <div>
    <h1 :style="{color:colorie}">Coucou</h1>
  </div>
  <Title title="Formulaire de Contact"/>
    <div>
      <TextInput name="name" label="Prénom"/>
      <TextInput name="lastname" label="Nom"/>
    </div>
    <div>
      <DateInput name="birthday" label="Date de Naissance"/>
    </div>
    <div>
      <TextArea :name="message" label="Message"/>
    </div>
    <div>
      <Select :name="Sexe"> 
      </Select>
    </div>
    <div>
      <Button msg="" v-on:validation="colorie='green'"/>
    </div>
    <div>
      <BtnForm type="submit" text="Envoyer"/>
      <BtnForm type="reset" text="Réinitialiser"/>
    </div>
   

</template>

<script>
import Title from './components/Title.vue';
import TextInput from './components/TextInput.vue';
import DateInput from './components/DateInput.vue';
import TextArea from './components/TextArea.vue';
import Select from './components/Select.vue';
import BtnForm from './components/BtnForm.vue';
import Button from './components/Button.vue';

export default {
  data () {
    return {
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
    BtnForm,
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
