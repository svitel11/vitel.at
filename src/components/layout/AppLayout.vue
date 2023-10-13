<script setup>
import {ref} from 'vue'
import AppHeader from "./AppHeader.vue";
import AboutMe from "../AboutMe.vue";
import WhatIDo from "../WhatIDo.vue";
import AppFooter from "./AppFooter.vue";
import MyStack from "../MyStack.vue";
import Social from "../Social.vue";
</script>

<template>
  <main id="main">

    <app-header></app-header>

    <div id="content">
      <about-me></about-me>
      <what-i-do></what-i-do>
      <my-stack></my-stack>
    </div>

    <social></social>

    <slot/>

    <app-footer></app-footer>
  </main>
</template>
