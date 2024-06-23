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

    <div class="green" v-if="(isWeekend = 1)">
      <h1>The Virtual Cafe is not open on the weekends</h1>
    </div>
    <div class="green" v-else>
      <h1>The Virtual Cafe is open between these times</h1>
      <h3>
        {{ new Date('2024-06-24' + 'T12:00:00.000Z').getHours() }}:{{
          new Date('2024-06-24' + 'T12:00:00.000Z').getMinutes()
        }}
        to {{ new Date('2024-06-24' + 'T20:00:00.000Z').getHours() }}:{{
          new Date('2024-06-24' + 'T20:00:00.000Z').getMinutes()
        }}
      </h3>
      Time is based on your current local time
    </div>
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
