<script setup>
import AboutData from '../components/AboutData.vue'
</script>

<template>
  <main>
    <AboutData />
    <div id="nav">
      <router-link :to="{ name: 'Home' }">Home</router-link> |
      <router-link :to="{ name: 'About' }">About</router-link>
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
