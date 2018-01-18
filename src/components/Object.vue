<template>
  <div>
    <template v-for="(item,index) in object">
      <formulate-object v-if="item.type==='object'" :object="item" v-bind:key="index"></formulate-object>
      <item v-else :item="item" v-bind:key="index"></item>
    </template>
  </div>
</template>

<script>
import Object from './Object2'
import Item from './Item'

export default {
  components: {'formulate-object': Object, 'item': Item},
  data () {
    return {
    }
  },
  props: ['object']
}
</script>
