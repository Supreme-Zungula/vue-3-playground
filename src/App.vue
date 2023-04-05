<script setup>
import BaseButton from "./components/BaseButton.vue";
const btnClicked = () => {
  console.log("Button clicked");
}
</script>

<template>
  <div>
    <h1 class="text-green-500 text-2xl text-center m-5">Vue playground</h1>
    <BaseButton @click="btnClicked" class="bg-green-400 rounded-md p-2 text-xl m-2"/>
  </div>
</template>

<style scoped>

</style>
