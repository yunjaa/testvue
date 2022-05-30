<template>
  <div class="hello">
    <cmTitle
      :type="1"
      :text="myInfo.heading"
    />

    <ul class="group-test">
      <li>
        <cmTitle text="<strong>이름</strong>입니다." />
        <cmText>{{ myInfo.text }}</cmText>
      </li>
      <li>
        <cmTitle
          :type="2"
          text="전화"
        />
        <cmText
          :type="1"
          :text="myInfo.tel"
        />
      </li>
    </ul>

    <div class="btn-wrap">
      <button @click="test('취소버튼 click!')">
        취소
      </button>
      <cmButton
        text="확인버튼"
        @onClick="test('확인버튼 click!')"
      />
    </div>
  </div>
</template> 

<script>
import cmTitle from '@/components/text/cmTitle';
import cmText from '@/components/text/cmText';
import cmButton from '@/components/button/cmButton';

export default {
  components: {
    cmTitle,
    cmText,
    cmButton,
  },
  props: { },
  data () {
    return {
      myInfo: {
        heading: 'Hello, World!',
        text: 'workyj',
        tel: '010-1234-5678'
      }
    }
  },
  methods: {
    test(msg) {
      console.log(msg);
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
