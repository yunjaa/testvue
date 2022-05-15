<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld :msg="msg" :name="name" :use="use"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }, 
  data: function() {
    return {
      msg: 'Welcome to Your Vue.js App',
      name: 'aa',
      use: true
    };
  }
}
</script>
