<script setup>
import { RouterView } from 'vue-router'
import HeaderDefault from './components/HeaderDefault.vue'
import FooterDefault from './components/FooterDefault.vue';
</script>

<template>
  <HeaderDefault class="header"></HeaderDefault>  

  <RouterView />

  <FooterDefault class="footer"></FooterDefault>
</template>

<style>
  .footer {
    bottom: 0;
    position: fixed;
  }
</style>
