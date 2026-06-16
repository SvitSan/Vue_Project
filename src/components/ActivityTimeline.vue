<script setup>
import ActivityItem from './ActivityItem.vue'

defineProps({
  activities: Array
})
</script>

<template>
  <div>
    <h3>Recent Activities</h3>

    <ActivityItem
      v-for="activity in activities"
      :key="activity.activityName"
      :activityName="activity.activityName"
      :date="activity.date"
      :type="activity.type"
    />
  </div>
</template>