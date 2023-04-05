<template>
  <div class="bg-zinc-800 h-full w-full">
    <h1 class="text-green-500 text-2xl text-center m-5">Vue playground</h1>
    <!-- Basic slot -->
    <FancyButton class="bg-sky-500 rounded-md p-2">Click</FancyButton>
    <!-- Named slot -->
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
    <!-- Scoped slot -->
    <FancyList :list="usersList">
     <template #item="{ name, surname }">
      <span class="bg-sky-500 rounded-md text-lime-500">{{ name }} {{ surname }}</span>
     </template>
    </FancyList>
  </div>
</template>

<script setup>
import { ref } from "vue";
import BaseLayout from "./components/BaseLayout.vue";
import FancyButton from "./components/FancyButton.vue";
import FancyList from "./components/FancyList.vue";

const usersList = ref([
  { name: "Yamkela", surname: "Zungula" },
  { name: "Buhle", surname: "Zungula" },
  { name: "Litha", surname: "Zungula" },
  { name: "Athi", surname: "Zungula" },
  { name: "Siyolo", surname: "Zungula" },
])
</script>

<style scoped>

</style>
