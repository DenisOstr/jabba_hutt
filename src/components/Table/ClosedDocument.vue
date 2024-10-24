<template>
  <sprite
    :position="{ x: positionX, y: positionY }"
    :scale="scale"
    :anchor="anchor"
    texture="/assets/textures/table/folder.png"
  />
</template>

<script setup lang="ts">
import { ref } from 'vue'

defineProps<{
  positionX: number
  positionY: number
}>()

const scale = ref(0.5)
const anchor = ref(0.5)
</script>
