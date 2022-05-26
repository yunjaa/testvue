<template>
  <div class="hello">
    <cmTitle :type="1" :heading="myInfo.heading" />
    <p v-if="use">{{ name }}</p>

    <ul class="group-test">
      <li>
        <cmTitle :type="2" heading="이름" />
        <cmText :type="1" :txt="myInfo.txt" />
      </li>
      <li>
        <cmTitle :type="2" heading="전화" />
        <cmText :type="2" :txt="myInfo.tel" />
      </li>
    </ul>

  </div>
</template>

<script>
import cmTitle from '@/components/text/cmTitle';
import cmText from '@/components/text/cmText';

export default {
  props: {
    name: String,
    use: Boolean
  },
  components: {
    cmTitle,
    cmText
  },
  data () {
    return {
      myInfo: {
        heading: 'Hello, World!',
        txt: 'workyj',
        tel: '010-1234-5678'
      }
    }
  }
}
</script>

<style lang="scss">
.group-test {
  width:50%;
  margin: 0 auto;
  padding: 0;
  border-bottom:1px solid gray;
  li {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding:10px 0;
    border-top:1px solid gray;
  }
  .basic{margin:0;}
}
</style>
