<script setup>
import { ref } from 'vue'
import PoliciesModal from './PoliciesModal.vue'

const isSkateTricksSelected = ref(false)
const isEasyChoiceSelected = ref(false)
const currentlySelectedApp = ref('')

const toggleSelection = app => {
  if (app === 'skate') {
    isSkateTricksSelected.value = true
    isEasyChoiceSelected.value = false
    currentlySelectedApp.value = 'Skate Tricks'
  } else {
    isSkateTricksSelected.value = false
    isEasyChoiceSelected.value = true
    currentlySelectedApp.value = 'Easy Choice'
  }
}

const resetCurrentlySelectedApp = () => {
  currentlySelectedApp.value = ''
  isSkateTricksSelected.value = false
  isEasyChoiceSelected.value = false
} 
</script>

<template>
  <div class="col-sm">
    <button type="button" @click="toggleSelection('skate')" class="btn btn-outline-primary me-1"
      :class="isSkateTricksSelected ? 'active' : 'inactive'" data-bs-toggle="modal" data-bs-target="#policy-modal">
      Skate Tricks
    </button>
    <button type="button" @click="toggleSelection('choice')" class="btn btn-outline-primary ms-1"
      :class="isEasyChoiceSelected ? 'active' : 'inactive'" data-bs-toggle="modal" data-bs-target="#policy-modal">
      Easy Choice
    </button>
    <PoliciesModal @reset="resetCurrentlySelectedApp" :modalTitle="currentlySelectedApp"
      :selectedAppForModal="currentlySelectedApp" />
  </div>
</template>

<style scoped></style>
