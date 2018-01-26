<template>
  <input v-bind:type="item.type" v-model="model"/>
</template>

<script>
export default {
  data () {
    return {}
  },
  props: ['item', 'model'],
  mounted () {}
}
</script>
