<template>
  <Application
    :width="windowWidth"
    :height="windowHeight"
    backgroundColor="#fff"
  >
    <BaseComponent :width="windowWidth" :height="windowHeight" />
  </Application>
</template>

<script setup lang="ts">
import { computed } from 'vue'
import { Application } from 'vue3-pixi'
import BaseComponent from './components/BaseComponent.vue'

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
