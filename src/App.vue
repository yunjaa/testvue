<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <aa msg="Welcome to Your Vue.js App" :use="true" :name="name"/>
    <label :for="'inp-'+ j" v-for="(item, j) in list" :key="j" >
      <input type="radio" :value="item.value" v-model="radioCheck" :id="'inp-'+ j" name="radioCheck">
      {{item.label}}
    </label>

    <br>
    {{radioCheck}}

    <div v-if="radioCheck == 10">
      은경
    </div>
    <div v-else-if="radioCheck == 11">
      성영
    </div>
  </div>
</template>

<script>
import aa from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    aa
  },
  data(){
    return {
      name: '안녕',
      cc: true,

      radioCheck: '',
      list: [{label:'김은경', value:'10'},{label:'김성영', value:'11'}]
    }
  }
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
