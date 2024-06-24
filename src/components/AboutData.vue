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

    <div class="green" v-if="isWeekend === 0">
      <h1>The Virtual Cafe is not open on the weekends</h1>
    </div>
    <div class="green" v-else>
      <h1>The Virtual Cafe is open between these times</h1>
      <h3>
        {{ new Date('2024-06-24' + 'T12:00:00.000Z').getHours() }}:{{
          new Date('2024-06-24' + 'T12:00:00.000Z').getMinutes().toString().padStart(2, '0')
        }}
        to {{ new Date('2024-06-24' + 'T20:00:00.000Z').getHours() }}:{{
          new Date('2024-06-24' + 'T20:00:00.000Z').getMinutes().toString().padStart(2, '0')
        }}
      </h3>
      Time is based on your current local time
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
