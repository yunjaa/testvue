<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
<<<<<<< Updated upstream
    <HelloWorld :msg="msg" :name="name" :use="use"/>
=======
    <HelloWorld :msg="msg" :name="name" :use="use" />
>>>>>>> Stashed changes
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
      name: 'workj',
      use: true
    };
  }
}
</script>
