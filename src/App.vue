<script setup lang='ts'>
import { themeColor } from './store'

const style = computed(() => ({
  '--theme-color': themeColor.value,
}))
</script>

<template>
  <div class="flex flex-col h-screen overflow-hidden bg" :style="style">
    <div class="h-full flex-auto overflow-overlay">
      <router-view />
    </div>
    <Progress />
  </div>
</template>
