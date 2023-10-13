<script setup>

import {ref} from "vue";

const imagesPath = ref("/src/assets/")

const social = ref([
  {
    name: "GitHub",
    url: "https://github.com/svitel11",
    uname: "svitel11",
    tag: '[#]',
    icon: imagesPath.value + "github.png"
  },
  {
    name: "LinkedIn",
    url: "https://www.linkedin.com/in/svitel11/",
    uname: "svitel11",
    tag: '@',
    icon: imagesPath.value + "linkedin.png"
  },
  {
    name: "Twitter",
    url: "https://twitter.com/svitel11",
    uname: "svitel11",
    tag: '#',
    icon: imagesPath.value + "twitter.png"
  }]
)

</script>

<template>
  <div class="social">
    <h1 class="title-tag"><span>Social Media</span></h1>

    <div class="social-items">
      <div class="social-item" v-for="item in social" :key="item.name">
        <img class="social-item-icon" :src="item.icon" :alt="item.name">
        <a :href="item.url" target="_blank" rel="noopener noreferrer"><span class="">{{item.tag}}</span>{{ item.uname }}</a>
      </div>
    </div>
  </div>
</template>