<template>
  <div>
    <input type="radio" :name="label" :value="label" @click="onChange" :checked="radio === label"/>{{label}}
  </div>
</template>

<script>
export default {
  model: {
    prop: 'radio',
    event: 'click'
  },
  props: {
    label: String,
    radio: String
  },
  methods: {
    onChange(){
      this.$emit('click', this.label)
      this.$emit('onChange')
    }
  },
  mounted() {
    console.log(this.label, this.radio);
  },
  destroyed() {
    console.log('触发了销毁周期');
  },
}
</script>
<style lang='scss' scoped>

</style>