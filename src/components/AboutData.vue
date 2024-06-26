<script setup>
import WelcomeItem from './WelcomeItem.vue'
</script>

<template>
  <WelcomeItem>
    <template #heading>About Us:</template>

    <div class="green">
      <h1>Some info</h1>
      <h3 class="info_text">
        <p>1, 2, 3, 4, 5, 6, 7, 8</p>
      </h3>
    </div>
  </WelcomeItem>
</template>

<style scoped>
a,
.green {
  color: white;
  font-size: 20px;
  text-shadow:
    0.07em 0 black,
    0 0.07em black,
    -0.07em 0 black,
    0 -0.07em black;
}

h3 {
  color: white;
  font-size: 90px;
  text-shadow:
    0.07em 0 black,
    0 0.07em black,
    -0.07em 0 black,
    0 -0.07em black;
}
</style>
