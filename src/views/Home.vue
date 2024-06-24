<script setup>
import HelloWorld from '../components/HelloWorld.vue'
import TheWelcome from '../components/TheWelcome.vue'
</script>

<template>
  <header>
    <img alt="logo" class="logo" src="../assets/1_112.png" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="Welcome to The Virtual Cafe" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

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

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    align-items: center;
    justify-content: center;
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
    align-items: center;
    justify-content: center;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
