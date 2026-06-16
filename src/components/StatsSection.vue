<script setup>
import StatCard from './StatCard.vue'

defineProps({
  stats: Array
})
</script>

<template>
  <div>
    <StatCard
      v-for="stat in stats"
      :key="stat.title"
      :title="stat.title"
      :value="stat.value"
      :icon="stat.icon"
    />
  </div>
</template>