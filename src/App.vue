<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld v-model="msg" />
    <MyModel v-model="radio" label="radio1" @onChange="onChange"></MyModel>
    <MyModel v-model="radio" label="radio2" @onChange="onChange"></MyModel>
    <customModel v-model="value1" :value1="value1"></customModel>
    <div>{{value1}}</div>
    <div>{{msg}}</div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import MyModel from './components/MyModel.vue'
import customModel from './components/customModel.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    MyModel,
    customModel
  },
  data() {
    return {
      msg: '',
      radio: 'radio1',
      value1: ''
    }
  },
  methods: {
    onChange(){
      // console.log(this.radio);
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
