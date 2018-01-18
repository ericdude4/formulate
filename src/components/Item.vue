<template>
  <input v-bind:type="item.type"/>
</template>

<script>
export default {
  data () {
    return {}
  },
  props: ['item']
}
</script>
