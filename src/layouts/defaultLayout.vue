<template>
  <div class="container">
    <defaultHeader></defaultHeader>
    <slot></slot>
    <defaultFooter></defaultFooter>
  </div>
</template>

<script>
import defaultHeader from '@/components/layout/defaultHeader.vue';
import defaultFooter from '@/components/layout/defaultFooter.vue';

export default {
  name: 'defaultLayout',
  components: {
    defaultHeader,
    defaultFooter
  }
}
</script>

<style scoped>

</style>