<template>
  <text :anchor="0.5" :x="width / 2" :y="height / 2">Welcome</text>
</template>

<script setup lang="ts">
defineProps<{
  width: number
  height: number
}>()
</script>
