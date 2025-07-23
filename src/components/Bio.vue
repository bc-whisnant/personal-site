<script setup>
import Contact from './Contact.vue';
import Policies from './Policies.vue';

</script>

<template>

  <div class="col-sm mb-5">
    <h2>Brandon Whisnant</h2>
    <h4>Software Engineer</h4>
    <p>Hi, I'm Brandon. I'm a software engineer but really I'm just a person that likes to tinker with things. I was born to be an engineer and was lucky enough to realize this at a rather young age.
      Programming has taken me places that I never thought I would go. My main goal is to just keep writing code and
      growing as a
      developer. After a decade of experience I'm as passionate as ever and ready for whatever challenges come my way.
    </p>
    <div class="mt-2">
      <Contact />
    </div>
    <div class="mt-4">
      <p>Below are the privacy policies for the iOS apps I've created. Yes, these are only here because Apple complained about it.</p>
      <Policies />
    </div>
  </div>
  <div class="bio-img col-sm d-flex flex-column justify-content-center align-items-center">
    <img src="../assets/b-gregg.jpeg" class="rounded-circle" alt="Brandon and his wonderful cat Gregg">
  </div>


</template>

<style scoped>
.bio-img img {
  height: 300px;
}
</style>
