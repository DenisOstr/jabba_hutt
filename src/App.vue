<template>
  <Application
    :width="windowWidth"
    :height="windowHeight"
    backgroundColor="#fff"
  >
    <TableComponent :width="windowWidth / 2" :height="windowHeight / 2" />
  </Application>
</template>

<script setup lang="ts">
import { computed } from 'vue'
import { Application } from 'vue3-pixi'
import TableComponent from './components/table/TableComponent.vue'

const windowWidth = computed(() => {
  return window.innerWidth
})

const windowHeight = computed(() => {
  return window.innerHeight
})
</script>

<style>
body {
  padding: 0;
  margin: 0;
}
</style>
