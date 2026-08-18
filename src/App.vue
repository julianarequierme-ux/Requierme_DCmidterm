<script setup>
import FeedbackForm from './components/FeedbackForm.vue'
import FeedbackDisplyForm from './components/FeedbackDisplay.vue'
</script>

<template>
  <FeedbackForm />
  <h1>Feedback Form</h1>
  <FeedbackDisplyForm :feedback="{
    name: 'Juliana Requierme',
    studentID: '2023-00001',
    email: 'juliana.requierme@example.com',
    Course: ['BSIT', 'BSCS', 'BSIS'],
    Rating: [1, 2, 3, 4, 5],
    Recommendation: [true, false],
    Feedback: 'This is a feedback message'
  }" />
</template>