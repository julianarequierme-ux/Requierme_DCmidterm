<script setup>
import { ref }  from 'vue'

const  StudentName = ref('');
const StudentID = ref('');
const Email = ref('');
const Course= ref('');
const Rating = ref('');
const Recommendation = ref('');
const Feedback = ref({
    StudentName: '',
    StudentID: '',
    Email: '',
    Course: '',
    Rating: '',
    Recommendation: false,
    Feedback: ''
});

</script>

<template>
    <div class="feedback-form">
        <h2>Feedback Form</h2>
        <form @submit.prevent="submitForm">
            <div>
                <label for="StudentName">Student Name:</label>
                <input type="text" id="StudentName" v-model="Feedback.StudentName" required />
            </div>

            <div>
                <label for="StudentID">Student ID:</label>
                <input type="text" id="StudentID" v-model="Feedback.StudentID" required />
            </div>

            <div>
                <label for="Email">Email:</label>
                <input type="email" id="Email" v-model="Feedback.Email" required />
            </div>

            <div>
                <label for="Course">Course:</label>
                <input type="text" id="Course" v-model="Feedback.Course" required />
            </div>

            <div>
                <label for="Rating">Rating (1-5):</label>
                <input type="number" id="Rating" v-model.number="Feedback.Rating" min="1" max="5" required />
            </div>

            <div>
                <label for="Recommendation">Would you recommend this course?</label>
                <input type="checkbox" id="Recommendation" v-model="Feedback.Recommendation" />
            </div>

            <div>
                <label for="Feedback">Additional Feedback:</label>
                <textarea id="Feedback" v-model="Feedback.Feedback"></textarea>
            </div>

            <button type="submit">Submit</button>
        </form>
    </div>
        </template>
