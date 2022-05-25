<template>
  <div :type="type">
    {{ txt }}
  </div>
</template>
<script>
// import { cmText } from '@vue/cmText'

export default {
  name: 'cmText',
  props: {
    txt: String,
    type: Number 
  }
}
</script>
<style scoped>

</style>