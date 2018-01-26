<template>
  <div>
    <template v-for="(struct,index) in structure">
      <formulate v-if="struct.type==='object'" :structure="struct.structure" :model="model[struct.key]" :key="index"/>
      <item v-else-if="struct.type!=='object'" :item="struct" :model="model[struct.key]" :key="index"/>
    </template>
  </div>
</template>

<script>
import Formulate from '@/components/Formulate'
import Item from './Item'

export default {
  name: 'formulate',
  components: {'formulate': Formulate, 'item': Item},
  data () {
    return {}
  },
  mounted () {
    if (!this.model) console.log('Inconsistent structure.key to model.key relationship')
  },
  props: ['structure', 'model']
}
</script>
