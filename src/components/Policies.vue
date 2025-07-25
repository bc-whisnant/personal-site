<script setup>
import { ref } from 'vue'
import PoliciesModal from './PoliciesModal.vue'
import { defineProps } from 'vue'

defineProps({
  windowIsSmall: Boolean
})

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

const buttons = [
  {
    app: 'choice',
    text: 'Easy Choice'
  },
  {
    app: 'skate',
    text: 'Skate Tricks'
  },
]

</script>

<template>
  <div class="col-lg mb-2">
    <h6 class="mb-4">Privacy Policies</h6>
    <button v-for="button in buttons" 
      @click="toggleSelection(button.app)" 
      :class="['btn', 'btn-lg', 'policy-btn', 'me-1', windowIsSmall && 'mb-4 w-100', button.app === 'skate' ? 'ms-1' : '']" data-bs-toggle="modal" data-bs-target="#policy-modal"
    >
      {{ button.text }}
    </button>

    <PoliciesModal @reset="resetCurrentlySelectedApp" :modalTitle="currentlySelectedApp"
      :selectedAppForModal="currentlySelectedApp" />
  </div>
</template>

<style scoped>
.policy-btn,
.policy-btn:hover {
  border-radius: 2.5rem;
  background-color: rgb(222, 139, 93);
  color: rgb(255, 255, 255);
  background-image: linear-gradient(243deg, rgb(140, 81, 214) 0%, rgba(222, 139, 93, 0.008) 74%);
}
</style>
