<template>
  <div class="hello">
    <input type="text" :value="value" @input="onInput">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    value: String
  },
  methods: {
    onInput(e){
      this.$emit('input', e.target.value)
    }
  },
  data() {
    return{

    }
  },
  mounted() {
    
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
