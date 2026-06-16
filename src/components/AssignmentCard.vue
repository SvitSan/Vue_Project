<script setup>
defineProps({
  title: String,
  dueDate: String,
  status: String
})
</script>

<template>
  <div class="card">
    <h4>{{ title }}</h4>

    <p>Due: {{ dueDate }}</p>

    <p>Status: {{ status }}</p>
  </div>
</template>

<style scoped>
.card {
  border: 1px solid #ddd;
  padding: 15px;
  margin-bottom: 10px;
}
</style>