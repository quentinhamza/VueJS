<template>
<div>

  <h1>User Infos</h1>
  <div class="user">
    <div>
      {{info[0].owner.login}}
    </div>
    <div>
      {{info[0].owner.id}}
    </div>
    <div>
        <img src="{{info[0].owner.avatar_url}}">
    </div>
  </div>
</div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'APIGitHub',
  data () {
    return {
      info: null,
    }
  },
  mounted () {
    axios
      .get('https://api.github.com/users/quentinhamza/repos')
      .then((results) => (this.info = results.data))
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
