<script setup>
import CoffeePlan from '../components/CoffeePlan.vue'
import { ref } from 'vue'
const plans = ref(['The Single', 'The Curious', 'The Addict', 'The Hacker'])

const selectCoffeePlan = ref()

function handleSelectedCoffeePlan(name) {
  selectCoffeePlan.value = name
}
</script>

<template>
  <div class="plans">
    {{ selectCoffeePlan }}
    <CoffeePlan
      v-for="plan in plans"
      :key="plan"
      :name="plan"
      :selected="plan === selectCoffeePlan"
      @selected="handleSelectedCoffeePlan"
    />
  </div>
</template>
