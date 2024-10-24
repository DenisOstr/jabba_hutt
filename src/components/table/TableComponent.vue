<template>
  <sprite
    :width="width"
    :height="height"
    :position="{ x: width, y: height }"
    :scale="{ x: 2, y: 1.5 }"
    :anchor="0.5"
    texture="/assets/textures/table/table.jpg"
  />

  <ClosedDocumentComponent
    v-for="(doc, index) in docs"
    :key="doc.id"
    :width="width"
    :height="height"
    :positionX="width + 50 * index"
    :positionY="height / 2"
  />
</template>

<script setup lang="ts">
import ClosedDocumentComponent from './ClosedDocumentComponent.vue'

defineProps<{
  width: number
  height: number
}>()

const docs = [
  {
    id: 1,
    name: 'John Doe',
  },
  {
    id: 2,
    name: 'Jane Doe',
  },
]
</script>
