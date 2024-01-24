<script setup>
import { RouterView } from 'vue-router'
import FooterItem from './components/FooterItem.vue'
</script>

<template>
  <div class="container">
    <RouterView />
    <div class="mt-5">
      <footer-item />
    </div>
  </div>
</template>

<style></style>
