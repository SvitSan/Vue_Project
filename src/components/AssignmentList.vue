<script setup>
import AssignmentCard from './AssignmentCard.vue'

defineProps({
  assignments: Array
})
</script>

<template>
  <div>
    <h3>Upcoming Assignments</h3>

    <AssignmentCard
      v-for="assignment in assignments"
      :key="assignment.title"
      :title="assignment.title"
      :dueDate="assignment.dueDate"
      :status="assignment.status"
    />
  </div>
</template> 