<script setup>
import { defineProps, } from 'vue'
import Contact from './Contact.vue';
import Policies from './Policies.vue';

defineProps({ 
  windowIsSmall: Boolean
})

</script>

<template>
  <div class="card" :style="[windowIsSmall ? { width: '20rem' } : { width: '35rem' }]">
    <div class="card-body">
      <img class="card-img-top rounded-circle mb-2" src="../assets/b-gregg.jpeg" alt="Brandon and his wonderful cat Gregg">
      <h4 class="card-job-title">Software Engineer</h4>
      <h2 class="title">Brandon Whisnant</h2>
      <p class="card-text">I build things with code. I specialize in frontend development and have spent a decade solving complex problems. </p>
      <p class="card-text">This site is mainly to store privacy policies for my iOS apps that I develop as a hobby.</p>
      <Contact :windowIsSmall="windowIsSmall" />
      <div>
        <Policies :windowIsSmall="windowIsSmall" />
      </div>
    </div>
  </div>
</template>

<style scoped>

.card {
  background-color: rgb(40, 39, 46) !important;
  border:2px solid gray;
  border-radius: 2rem !important;
}

.card-body img {
  height: 100px;
  width: 100px;
  text-align: left;
}

.title {
  font-size: 2.25em;
  color: white;
}

.card-job-title {
  background-color: rgb(222, 139, 93);
  color: rgb(255, 255, 255);
  background-image: linear-gradient(243deg, rgb(140, 81, 214) 0%, rgba(222, 139, 93, 0.008) 74%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.card-text {
  color: rgba(255, 255, 255, 0.61);
}

</style>
