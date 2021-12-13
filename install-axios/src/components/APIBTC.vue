<template>
  <div>
    <h1>Bitcoin Price Index</h1>
    <div v-for="currency in info" :key="currency" class="currency">
      {{ currency.description }}:
      <span class="lighten">
        <span v-html="currency.symbol"></span>{{ currency.rate_float }}
      </span>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'APIBTC',
  data () {
    return {
      info: null,
    }
  },
  mounted () {
    axios
      .get('https://api.coindesk.com/v1/bpi/currentprice.json')
      .then(response => (this.info = response.data.bpi))
  },
}


</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
