<script setup>
import WelcomeItem from './WelcomeItem.vue'
</script>

<template>
  <WelcomeItem>
    <template #heading>Opening hours</template>

    <router-link :to="{ name: 'About' }"
      ><p class="green">You can find our current opening hours on the about page</p></router-link
    >
  </WelcomeItem>
</template>

<style scoped>
a,
.green {
  color: white;
  font-size: 40px;
  text-shadow:
    0.07em 0 black,
    0 0.07em black,
    -0.07em 0 black,
    0 -0.07em black;
}
</style>
