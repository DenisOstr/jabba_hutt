<template>
  <sprite
    :width="width"
    :height="height"
    :position="{ x: positionX, y: positionY }"
    :scale="{ x: 0.5, y: 0.5 }"
    :anchor="0.5"
    texture="/assets/textures/table/folder.png"
  />
</template>

<script setup lang="ts">
defineProps<{
  width: number
  height: number
  positionX: number
  positionY: number
}>()
</script>
