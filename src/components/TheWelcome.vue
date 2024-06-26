<script setup>
import WelcomeItem from './WelcomeItem.vue'
</script>

<script>
export default {
  methods: {
    isWeekend() {
      var myDate = new Date()
      if (!(myDate.getDay() % 6)) {
        return 0
      } else {
        return 1
      }
    }
  }
}
</script>

<template>
  <WelcomeItem>
    <template #heading>Opening hours</template>
    <div v-if="isWeekend === 0">
      <h1>The Virtual Cafe is not open on the weekends</h1>
    </div>
    <div v-else>
      <h3 class="timezone">
        {{ new Date('2024-06-24' + 'T12:00:00.000Z').getHours() }}:{{
          new Date('2024-06-24' + 'T12:00:00.000Z').getMinutes().toString().padStart(2, '0')
        }}
        to {{ new Date('2024-06-24' + 'T20:00:00.000Z').getHours() }}:{{
          new Date('2024-06-24' + 'T20:00:00.000Z').getMinutes().toString().padStart(2, '0')
        }}
      </h3>
      <router-link :to="{ name: 'About' }">Time is based on your current local time </router-link>
    </div>
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

.timezone {
  color: white;
  font-size: 90px;
  text-shadow:
    0.07em 0 black,
    0 0.07em black,
    -0.07em 0 black,
    0 -0.07em black;
}
</style>
