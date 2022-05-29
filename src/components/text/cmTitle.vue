<template>
  <h2
    v-if="$slots.default"
    class="head"
    :class="getType(type)"
    v-html="text"
  />
  <h3
    v-else
    class="head"
    v-html="text"
  />
</template>
<script>
export default {
  name: 'CmTitle',
  props: {
    text: String,
    type: {
      type: Number,
      require: false,
      default: 1
    }
  },
  data () {
    return {
    };
  },
  methods: {
    getType() {
      return 'head-'+this.type;
    }
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