<template>
  <div>
     <h1>Reactive count: {{ state.count }}</h1> 
     <h1>Ref count: {{ count }}</h1>
     <button @click="increment">Increment</button>
  </div>
</template>
<script>
import { reactive, ref } from 'vue';
export default {
  setup() {
    const state = reactive({ count: 1 });
    const count = ref(0);

    function increment() {
      state.count++;
      count.value++;
    }
    return {
      state,
      count,
      increment
    }
  }
}
</script>
<style lang="">
  
</style>