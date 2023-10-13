<script setup>

import {ref} from "vue";

const imagesPath = ref("/src/assets/")

const bracketOpen = ref(imagesPath.value + "bracket_open.webp")
const bracketClose = ref(imagesPath.value + "bracket_close.webp")

const images = ref({
  vuejs: imagesPath.value + "vuejs.svg",
  javascript: imagesPath.value + "javascript.png",
  php: imagesPath.value + "php.png",
  laravel: imagesPath.value + "laravel.png",
  linux: imagesPath.value + "linux.png"
})

</script>

<template>

  <div class="my-stack">
    <h1 class="title-tag"><span>Stack</span></h1>

    <div class="bracket-open-box">
      <div class="fake-lines">- -</div>
      <img class="bracket-open" :src="bracketOpen" alt="bracket open" />
    </div>


    <div class="stack-image-box" v-for="pl in Object.keys(images)">
      <div class="fake-lines">- - - - -</div>
      <img
          class="stack-image"
           :src="images[pl]" :alt="pl" />
    </div>

    <div class="bracket-close-box">
      <div class="fake-lines">- -</div>
      <img class="bracket-close" :src="bracketClose" alt="bracket close" />
    </div>
  </div>
</template>