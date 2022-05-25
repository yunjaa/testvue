<template>
  <div class="container" :class="classObject">
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
  },
  data: function() {
  return {
      classObject : [
      ]
    };
  }
}
</script>

<style scoped>

</style>