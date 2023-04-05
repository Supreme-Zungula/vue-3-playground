<script setup>
import BaseLayout from "./components/BaseLayout.vue";
import FancyButton from "./components/FancyButton.vue";
</script>

<template>
  <div class="bg-zinc-800 h-full w-full">
    <h1 class="text-green-500 text-2xl text-center m-5">Vue playground</h1>
    <FancyButton class="bg-sky-500 rounded-md p-2">Click</FancyButton>
    <BaseLayout>
      <template #header>
        <h1>Header Slot</h1>
      </template>
      <template #default>
         <p>Main slot</p>
      </template>
      <template #footer>
        <p>Footer slot</p>
      </template>
    </BaseLayout>
  </div>
</template>

<style scoped>

</style>
