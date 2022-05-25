<template>
  <div>
    <h2 v-if="type === 1" :class="titleClass">{{ heading }}</h2>
    <h3 v-if="type === 2" :class="titleClass">{{ heading }}</h3>
    <h4 v-if="type === 3" :class="titleClass">{{ heading }}</h4>
    <h5 v-if="type === 4" :class="titleClass">{{ heading }}</h5>
  </div>
</template>
<script>
export default {
  name: 'cmTitle',
  props: {
    heading: String,
    type: Number
  },
  data () {
    return {
      titleClass:'head head-'+this.type
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