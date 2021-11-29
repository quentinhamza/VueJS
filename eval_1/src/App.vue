<template>
  <div>
    <DateBtn name="date" label="Select a day : "/>
    </div>
  <div>
    <p>Choose one of the available timeslots</p>
    <RadioBtn name="heure" label="12h" />
  </div>
  <div>
    <strong>Can't find the time you are looking for ?</strong>
  </div>
  <div>
    <p>You have been added to the waiting list</p>
  </div>
  <div>
    <strong>Informations about available timeslots</strong>
  </div>
  <div style="display: flex; justify-content: space-around;">
    <ul>
      <li style="text-align: justify;">Regular slots (FREE)</li>
      <li style="text-align: justify; color: green">Premium slots (INR 134)</li>
      <li style="text-align: justify; color: purple">Prime slots (INR 254)</li>
    </ul>
  </div>
  <div>
      <ValidationBtn style="background-color:orange; border:none; padding: 5px 300px" type="submit" text="Valider" v-on:validation="colorie='green'" />
  </div>
  </template>

<script>
import RadioBtn from './components/RadioBtn.vue';
import DateBtn from './components/DateBtn.vue';
import ValidationBtn from './components/ValidationBtn.vue'

export default {
  name: 'App',
  components: {
    RadioBtn,
    DateBtn,
    ValidationBtn,
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
</style>
