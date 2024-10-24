<template>
  <sprite
    :position="{ x: width, y: height }"
    :scale="scale"
    :anchor="anchor"
    texture="/assets/textures/table/table.jpg"
  />

  <ClosedDocument
    :key="doc.id"
    :positionX="calcPosX(index)"
    :positionY="calcPosY()"
    v-for="(doc, index) in docs"
  />
</template>

<script setup lang="ts">
import { ref } from 'vue'
import ClosedDocument from './ClosedDocument.vue'

const props = defineProps<{
  width: number
  height: number
}>()

const scale = ref({
  x: 2,
  y: 1.5,
})
const anchor = ref(0.5)
const docs = ref([
  {
    id: 1,
    name: 'John Doe',
  },
  {
    id: 2,
    name: 'Jane Doe',
  },
])

function calcPosX(index: number) {
  return props.width + 50 * index
}

function calcPosY() {
  return props.height / 2
}
</script>
