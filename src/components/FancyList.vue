<template>
  <h2 v-if="list.length === 0">List empty</h2>
  <ul v-else>
    <li v-for="(item, index) in list" :key="index">
      <slot name="item" v-bind="item"></slot>
    </li>
  </ul>
</template>
<script>
export default {
  props: {
    list: {
      type: Array,
      required: true,
      default: []
    }
  }
}
</script>
<style>
  
</style>