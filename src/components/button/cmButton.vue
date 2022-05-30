<template>
  <button
    type="button"
    class="btn"
    @click.stop="onClick"
    v-html="text"
  />
</template>

<script>
export default {
  naem: 'cmButton',
  props: {
    text: {
      type: String,
      default: '확인'
    }
  },
  methods: {
    onClick() {
      this.$emit('onClick');
    }
  }
}
</script>

<style lang="scss" scoped>
$primary: blue;
$secondary: red;
.btn- {
  &primary {
    background-color: $primary;
  }
  &secondary {
    background-color: $secondary;
  }
}
</style>