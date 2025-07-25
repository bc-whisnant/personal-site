<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import Bio from './components/Bio.vue'

const windowWidth = ref(window.innerWidth)
const windowIsSmall = ref(false)

onMounted(() => {
  window.addEventListener('resize', handleResize)
  handleResize()
})

onUnmounted(() => {
  window.removeEventListener('resize', handleResize)
})

const handleResize = () => {
  windowWidth.value = window.innerWidth

  if (windowWidth.value < 501) {
    windowIsSmall.value = true
  } else {
    windowIsSmall.value = false
  }
} 

</script>

<template>
  <div class="container">
    <div class="row">
       <Bio :windowIsSmall="windowIsSmall" />
    </div>
  </div>
  
</template>

<style scoped>

</style>
