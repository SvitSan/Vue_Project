  <script setup>
defineProps({
  avatar: String,
  fullName: String,
  email: String,
  batch: String,
  track: String
})
</script>

<template>
  <div>
    <img :src="avatar" width="100">

    <h2>{{ fullName }}</h2>

    <p>{{ email }}</p>

    <p>Batch: {{ batch }}</p>

    <p>Track: {{ track }}</p>
  </div>
</template>