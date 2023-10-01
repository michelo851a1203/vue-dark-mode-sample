<script setup lang="ts">
  import { useToggle, useDark , useColorMode } from '@vueuse/core'
  const colorMode = useColorMode();
  const isDark = useDark();
  const toggleDark = useToggle(isDark);
</script>

<template>
  {{ colorMode }}
  <button @click="toggleDark()">ToDarkOrLight</button>
  <div w-32 h-32 bg="blue-400 dark:red-600" rounded-full></div>
</template>

<style>
.dark {
  background-color: #4b5563;
}
</style>
