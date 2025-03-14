<script setup>
import {useDark, useToggle} from "@vueuse/core";
import NavBar from "@/views/NavBar.vue";

const isDark = useDark();
const toggleDark = useToggle(isDark);
</script>

<template>
  <NavBar/>


    <div
      class=" flex items-start justify-center shadow-md p-6 rounded-md bg-white dark:bg-slate-700 mt-20"
    >
      <div class="flex items-start sm:items-center mb-4">
        <h1 class="text-4xl flex-1 dark:text-white">
          Vue Tailwind Dark/Light Mode
        </h1>
      </div>
      <button
        @click="toggleDark()"
        class="py-2 px-4 bg-black text-white rounded-md dark:bg-white dark:text-black"
      >
       Toggle {{ isDark ? "Light" : "Dark" }}
      </button>
    </div>
</template>
