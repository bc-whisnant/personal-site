<script setup>

const props = defineProps({
  windowIsSmall: Boolean
})

const items = [
  {
    itemClass: 'me-1',
    link: '../assets/files/brandon-whisnant-software-engineer-resume.pdf',
    linkClass: 'btn btn-lg contact-btn',
    linkText: 'Resume',
    type: 'file'
  },
  {
    itemClass: 'ms-1 me-1',
    link: 'https://github.com/bc-whisnant',
    linkClass: 'btn btn-lg contact-btn',
    linkText: 'Github',
    type: 'link'
  },
  {
    itemClass: 'ms-1',
    link: 'https://www.linkedin.com/in/brandon-c-whisnant/',
    linkClass: 'btn btn-lg contact-btn',
    linkText: 'Linkedin',
    type: 'link'
  },
]
</script>

<template>
  <div class="contact mb-4">
    <h6 class="mb-4">Contact Info</h6>
    <ul class="d-flex" :class="[windowIsSmall && 'flex-column']">
      <li v-for="item in items" :class="[item.itemClass, windowIsSmall ? 'mb-4' : '']">
        <a :href="item.link" :class="[item.linkClass, windowIsSmall ? 'w-100' : '']"
          :download="item.type === 'file' ? 'brandon-whisnant-frontend-engineer.pdf' : null"
          :target="item.type === 'link' ? '_blank' : null">{{ item.linkText }}</a>
      </li>
    </ul>
  </div>
</template>
<style scoped>
a,
a:visited {
  text-decoration: none;
}


a:hover {
  color: white;
}

ul {
  padding-left: 0px;
}

li {
  list-style: none;
}

li .contact-btn {
  border-radius: 2.5rem;
  background-color: rgb(222, 139, 93);
  color: rgb(255, 255, 255);
  background-image: linear-gradient(243deg, rgb(140, 81, 214) 0%, rgba(222, 139, 93, 0.008) 74%);
}
</style>