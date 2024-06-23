<script setup>
import WelcomeItem from './WelcomeItem.vue'
</script>

<script>
export default {
  methods: {
    isWeekend(){
      var myDate = new Date();
      if(!(myDate.getDay() % 6)){
        return 0;
      }
      else {
        return 1;
      }
    },
    prettyDate2(time) {
      var date = new Date(parseInt(time));
      return date.toLocaleTimeString(navigator.language, {
        hour: '2-digit',
        minute:'2-digit'
    });
}
  }
}
</script>

<template>
  <WelcomeItem>
    <template #heading>Opening hours</template>

    <div class="green">
      <h1 v-if="isWeekend=1">
        The Virtual Cafe is not open on the weekends
      </h1>  
      <p>open on weekdays from 12pm to 8pm UTC</p><br>
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