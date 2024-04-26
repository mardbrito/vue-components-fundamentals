<script setup>
import CoffeePlan from '../components/CoffeePlan.vue'
import { ref } from 'vue'
const plans = ref(['The Single', 'The Curious', 'The Addict', 'The Hacker'])
</script>

<template>
  <div class="plans">
    <CoffeePlan v-for="plan in plans" :key="plan" :name="plan" />
  </div>
</template>
