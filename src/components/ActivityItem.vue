<script setup>
defineProps({
  activityName: String,
  date: String,
  type: String
})
</script>

<template>
  <div class="activity">
    <h4>{{ activityName }}</h4>

    <p>{{ date }}</p>

    <small>{{ type }}</small>
  </div>
</template>

<style scoped>
.activity {
  padding: 10px;
  border-bottom: 1px solid #ddd;
}
</style>