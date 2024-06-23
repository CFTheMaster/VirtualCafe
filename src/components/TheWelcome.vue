<script setup>
import WelcomeItem from './WelcomeItem.vue'
</script>

<template>
  <WelcomeItem>
    <template #heading>Opening hours</template>

    <router-link to="/about"><p class="green">You can find our current opening hours on the about me page</p></router-link>
  </WelcomeItem>
</template>

<style scoped>
  a,
  .green {
    text-decoration: none;
    text-align: center;
    color: #00ff00;
    transition: 0.4s;
    padding: 3px;
    background: content-box #6f373c;
  } 
</style>
