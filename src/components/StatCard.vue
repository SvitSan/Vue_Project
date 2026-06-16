<script setup>
defineProps({
  title: String,
  value: [String, Number],
  icon: String
})
</script>

<template>
  <div>
    <h3>{{ icon }}</h3>

    <p>{{ title }}</p>

    <strong>{{ value }}</strong>
  </div>
</template>