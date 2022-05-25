<template>
  <p class="basic" :class="txtClass">{{ txt }}</p>
</template>
<script>
export default {
  name: 'cmText',
  props: {
    txt: String,
    type: String 
  },
  data () {
    return {
      txtClass:'basic-'+this.type
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
    &-2{
      color: $txt-secondary;
    }
  }
}
</style>