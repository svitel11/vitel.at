<script setup>

import {onMounted, ref} from 'vue'

const isMob = ref(window.innerWidth <= 890)
const text = ref('Webentwicklung | Webdesign | Webhosting')

const delay = ref(100) // Adjust the delay between letters (in milliseconds)
const currentIndex = ref(0)
const textContent = ref('')

function typeLetter() {
  textContent.value = text.value.substring(0, currentIndex.value);
  currentIndex.value++;

  if (currentIndex.value <= text.value.length) {
    setTimeout(typeLetter, delay.value);
  }
}

onMounted(() => {
  if (!isMob.value)
    typeLetter()
  else
    textContent.value = '<span>Webentwicklung</span><span>Webdesign</span><span>Webhosting</span>'
})

</script>

<template>
  <div id="header">
    <img class="logo" src="../../assets/logo_vitel_xs.png" alt="Samuel Vitel logo"/>

    <div class="header-text" v-html="textContent"></div>
  </div>
</template>