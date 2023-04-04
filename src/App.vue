<template>
  <div>
    <h1>Template Refs</h1>
    <input type="text" ref="inputRef">
    <ul>
      <li v-for="(item, index) in list" :key="index" ref="itemRefs">{{ item }}</li>
    </ul>
  </div>
</template>
<script setup>
import { onMounted, ref } from 'vue';

const inputRef = ref(null)
const itemRefs = ref([])
const list = ref([1, 2, 3, 4, 5])

onMounted(() => {
  inputRef.value.focus();
  console.log(itemRefs.value);
})
</script>

<style scoped>
</style>
