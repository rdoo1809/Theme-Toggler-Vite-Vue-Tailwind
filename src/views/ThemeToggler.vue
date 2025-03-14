<script setup>
import { useDark, useToggle } from "@vueuse/core";

const isDark = useDark();
const toggleDark = useToggle(isDark);
</script>

<template>
  <div class="absolute bottom-0 right-0 m-4">

    <label class="relative inline-flex items-center cursor-pointer">

      <input type="checkbox" class="sr-only peer" @click="toggleDark()" />

      <div
          class="w-24 h-12 bg-gray-300 peer-focus:outline-none peer-focus:ring-2
             dark:bg-gray-700 rounded-full peer peer-checked:after:translate-x-12
             peer-checked:after:border-white after:content-[''] after:absolute
             after:top-1 after:left-1 after:w-10 after:h-10 after:bg-white after:border-gray-300
             after:border after:rounded-full after:transition-all peer-checked:bg-grey-700"
      >

      </div>
    </label>
  </div>
</template>