<template>
  <input type="text" :value="value1" @input="add">
</template>

<script>
export default {
  components: {},
  model: {
    // prop: 'value1',
    event: 'customInput'
  },
  props: {
    value1: String
  },
  methods: {
    add(e){
      this.$emit('customInput', e.target.value)
    }
  },
  watch: {
    value1(a, b){
      console.log(a, b);
    }
  }
}
</script>
<style lang='scss' scoped>

</style>
