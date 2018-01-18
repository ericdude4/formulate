<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
      <formulate :structure="structure"></formulate>
  </div>
</template>

<script>
import Formulate from './Formulate'

export default {
  name: 'HelloWorld',
  components: {'formulate': Formulate},
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      structure: [
        {type: 'text'},
        {type: 'datetime-local'},
        {type: 'number'},
        {
          type: 'object',
          structure: [
            {type: 'text'},
            {type: 'datetime-local'},
            {type: 'number'}
          ]
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
