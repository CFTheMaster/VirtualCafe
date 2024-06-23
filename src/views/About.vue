<script setup>
import AboutData from '../components/AboutData.vue'
</script>

<template>
    
    <main>
        <AboutData />
        <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
  </div>
    </main>
    
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