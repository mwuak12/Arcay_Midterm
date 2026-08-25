<script setup>
import { ref } from 'vue'

const emit = defineEmits(['studentSubmitted'])

const studentName = ref('')
const studentId = ref('')
const course = ref('')
const yearLevel = ref('')
const email = ref('')

const submitStudent = () => {
  const studentData = {
    name: studentName.value,
    studentId: studentId.value,
    course: course.value,
    yearLevel: yearLevel.value,
    email: email.value
  }

  emit('studentSubmitted', studentData)
  console.log('Student submitted: ', studentData)
}
</script>

<template>
  <form @submit.prevent="submitStudent">
   
      <label>Student Name: </label>
      <input
        v-model="studentName"
        type="text"
      />
      <br><br>
      <label>Student ID: </label>
      <input
        v-model="studentId"
        type="text"
      />
      <br><br>
      <label>Course: </label>
      <select v-model="course" required>
        <option>BSIT</option>
        <option>BSCS</option>
        <option>BSIS</option>
      </select>

      <div>
      <p>Year Level: </p>
      <label>
        <input
          v-model="yearLevel"
          type="radio"
          value="1st Year"
          
        />
        1st Year
      </label>

      <label>
        <input type="radio" value="2nd Year" v-model="yearLevel"/>2nd Year
      </label>
      <label>
        <input
          v-model="yearLevel"
          type="radio"
          value="3rd Year"
        />
        3rd Year
      </label>
      <label>
        <input
          v-model="yearLevel"
          type="radio"
          value="4th Year"
        />
        4th Year
      </label>
    <br><br>
      <label>Email: </label>
      <input
        v-model="email"
        type="email"
      />
    </div>
   <br>
    <button @click="submitStudent">Submit Student</button>
  </form>
  
</template>
