<template>
  <div class="contact mb-4">
    <h6 class="mb-4">Contact Info</h6>
    <ul class="d-flex">
      <li class="me-1">
        <a href="https://www.linkedin.com/in/brandon-c-whisnant/" class="btn btn-lg contact-btn" target="_blank">Linkedin</a>
      </li>
      <li class="ms-1">
        <a href="https://github.com/bc-whisnant" class="btn btn-lg contact-btn" target="_blank">Github</a>
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