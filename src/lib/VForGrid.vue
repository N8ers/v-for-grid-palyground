<template>
  <div>i am VForGrid</div>
  <!-- // figure out how to pass key in later -->
  <div v-for="item in data" :key="item.name">
    {{ item.name }}
    <slot :item="item.name"></slot>
  </div>
</template>

<script>
export default {
  name: 'VForGrid',
  props: {
    data: {
      type: Array,
      default: () => []
    },
    gridProps: {
      type: Object,
      default: () => {}
    }
  }
}
</script>

<style>
</style>
