<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
      <formulate :structure="structure" :model="model"/>
  </div>
</template>

<script>
import Formulate from './Formulate'

export default {
  components: {'formulate': Formulate},
  data () {
    return {
      msg: 'Vue Formulate',
      structure: [
        {type: 'text', key: 'name'},
        {type: 'number', key: 'age'},
        {type: 'datetime-local', key: 'birthday'},
        {
          type: 'object',
          key: 'fiance',
          structure: [
            {type: 'text', key: 'name'},
            {type: 'number', key: 'age'},
            {type: 'datetime-local', key: 'birthday'},
            {
              type: 'object',
              key: 'school',
              structure: [
                {type: 'text', key: 'name'},
                {type: 'text', key: 'city'},
                {type: 'datetime-local', key: 'date_of_enrollment'}
              ]
            }
          ]
        }
      ],
      model: {
        name: 'Eric',
        age: 24,
        birthday: 'October 17, 1993',
        fiance: {
          name: 'Rachel',
          age: 22,
          birthday: 'December 22, 1995',
          school: {
            name: 'Tyndale',
            city: 'Toronto',
            date_of_enrollment: 'September 5, 2013'
          }
        }
      }
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
