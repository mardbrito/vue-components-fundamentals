<script setup>
import { ref } from 'vue'
import CoffeePlan from './components/CoffeePlan.vue'

const plans = ref(['The Single', 'The Curious', 'The Addict', 'The Hacker'])
</script>

<template>
  <div class="content">
    <h1 class="title">Coffee Plans</h1>

    <h2 class="subtitle">
      We travel the world to source the very best single origin coffee for you
    </h2>

    <div class="plans">
      <CoffeePlan v-for="plan in plans" :key="plan" :name="plan" />
    </div>
  </div>
</template>
