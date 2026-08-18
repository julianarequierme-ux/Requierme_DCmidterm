<script setup>
import { ref } from 'vue'
const props = defineProps({
feedback: {
    type: Object,
    required: true}
})
const feedback = ref(props.feedback);
</script>

<template>
    <div class="feedback">
        <h2>Feedback Display</h2>
        <p><strong>Student Name:</strong> {{ feedback.StudentName }}</p>
        <p><strong>Student ID:</strong> {{ feedback.StudentID }}</p>
        <p><strong>Email:</strong> {{ feedback.Email }}</p>
        <p><strong>Course:</strong> {{ feedback.Course }}</p>
        <p><strong>Rating:</strong> {{ feedback.Rating }}</p>
        <p><strong>Recommendation:</strong> {{ feedback.Recommendation ? 'Yes' : 'No' }}</p>
        <p><strong> Feedback:</strong> {{ feedback.Feedback }}</p>
    </div>
</template>