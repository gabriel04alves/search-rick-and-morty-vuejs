<script setup>
import { RouterView } from 'vue-router'
import HeaderDefault from './components/HeaderDefault.vue'
import FooterDefault from './components/FooterDefault.vue';
</script>

<template>
  <HeaderDefault class="header"></HeaderDefault>  

  <RouterView class="view"/>

  <FooterDefault class="footer"></FooterDefault>
</template>

<style>
  .view {
    height:max-content;
  }
  .footer {
    bottom: 0;
    position: fixed;
  }
</style>
