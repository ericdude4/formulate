<template>
  <div>
    <template v-for="(item,index) in structure">
      <formulate-object v-if="item.type==='object'" :object="item" v-bind:key="index"/>
      <item v-else :item="item" v-bind:key="index"/>
    </template>
  </div>
</template>

<script>
import Object from './Object'
import Item from './Item'

export default {
  components: {'formulate-object': Object, 'item': Item},
  data () {
    return {}
  },
  props: ['structure']
}
</script>
