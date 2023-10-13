<script setup>

import {ref} from "vue";

const services = ref([
  'Webseiten',
  'Webapplikationen',
  'Webshops',
  'Webdesign',
  'Upgrades und Verbesserungen von bestehenden Websites und Webapplikationen',
  'APIs',
  'Serverdienste wie das Bereitstellen von Webapplikationen auf Plattformen wie Shared Hosting oder virtuellen Maschinen (Azure, Amazon, etc.)',
  'Integration von Werbetags'
])

</script>

<template>
  <div class="what-i-do">
    <h1 class="title-tag"><span>Was mache ich</span></h1>
    <ul>
      <li
          class="ml-2 my-1"
          v-for="service in services" :key="service">{{service}}</li>
    </ul>
  </div>
</template>