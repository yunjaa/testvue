<template>
  <p
    v-if="$slots.default"
    class="basic"
    :class="getType(type)"
  >
    <slot />
  </p>
  <p
    v-else
    class="basic"
    :class="getType(type)"
    v-html="text"
  />
</template>
<script>
export default {
  name: 'CmText',
  props: {
    text: String,
    type: {
      type: Number,
      default: 1
    }
  },
  data () {
    return {
    };
  },
  methods: {
    getType() {
      return 'basic-'+this.type;
    }
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