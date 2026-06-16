<script setup>
defineProps({
  courseName: String,
  instructor: String,
  progress: Number
})
</script>

<template>
  <div class="course-info">
    <h2>{{ courseName }}</h2>

    <p>Instructor: {{ instructor }}</p>

    <p>Progress: {{ progress }}%</p>

    <progress :value="progress" max="100"></progress>
  </div>
</template>

<style scoped>
.course-info {
  padding: 20px;
  border: 1px solid #ddd;
}
</style>