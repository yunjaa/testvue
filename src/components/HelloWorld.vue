<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2 v-if="use">{{ name }}</h2>
    <p>테스트 중입니다.</p>
    <p>테스트 중입니다.</p>
    <p>테스트 중입니다.</p>
    <p>테스트 중입니다.</p>

    
    <cmText :type="1" :txt="txt" />
  </div>
</template>

<script>
import cmText from '@/components/text/cmText';

export default {
  props: {
    msg: String,
    name: String,
    use: Boolean
  },
  components: { 
    cmText
  },
  data () {
    return {
      txt: '안녕~!'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
