<script setup>
import { RouterView } from 'vue-router'
import HeaderDefault from './components/HeaderDefault.vue'
import FooterDefault from './components/FooterDefault.vue';
</script>

<template>
  <HeaderDefault class="header"></HeaderDefault>  

  <RouterView class="content"/>

  <FooterDefault class="footer"></FooterDefault>
</template>

<style>
  .content {
    height: 70%;
  }
</style>
