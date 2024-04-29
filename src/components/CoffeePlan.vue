<script setup>
const props = defineProps({
  name: { type: String, default: 'Default Plan' },
  selected: { type: Boolean, default: false }
})

const emit = defineEmits(['selected'])

function selectPlan() {
  emit('selected', props.name)
}
</script>

<template>
  <div class="plan" @click="selectPlan" :class="{ 'active-plan': selected }">
    <div class="description">
      <span class="title"> {{ name }} </span>
    </div>
  </div>
</template>
