<template>
  <div>
    <h2 class="head" :class="getType(type)">{{ heading }}</h2>
  </div>
</template>
<script>
export default {
  name: 'cmTitle',
  props: {
    heading: String,
    type: Number
  },
  methods: {
    getType() {
      return 'head-'+this.type;
    }
  },
  data () {
    return {
    };
  }
}
</script>
<style lang="scss">
.head{
  margin: 0;
  font-weight: bold;
  &-1{
    font-size: 20px;
  }
  &-2{
    font-size: 18px;
  }
  &-3{
    font-size: 16px;
  }
}
</style>