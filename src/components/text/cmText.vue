<template>
  <p class="basic" :class="getType(type)">{{ txt }}</p>
</template>
<script>
export default {
  name: 'cmText',
  props: {
    txt: String,
    type: Number
  },
  methods: {
    getType() {
      return 'basic-'+this.type;
    }
  },
  data () {
    return {
    };
  }
}
</script>
<style lang="scss">
$txt-basic: #111;
$txt-primary: blue;
$txt-secondary: red;
p {
  &.basic{
    color: $txt-basic;
    &-primary,
    &-1{
      color: $txt-primary;
    }
    &-secondary,
    &-2{
      color: $txt-secondary;
    }
  }
}
</style>