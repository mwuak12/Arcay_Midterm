<script setup>
// import {ref} from 'vue'

// const studentName = ref('')
// const name = ref('')
// const message = ref('')

// function submitForm() {
//     message.value = `Hello, ${name.value}!`
// }
// const email = ref('')
// function register() {
//     alert("Registration successful!")
// }
// const acceptedTerms = ref('')
// const course = ref('')
// const props = defineProps({
//     studentName: String
// })
const emit = defineEmits(['submitStudent'])

  function saveStudentName() {
    emit('save')
  }
  function submitStudent() {
    emit('submitStudent', {
      name: Ampong,
      age: 20
    })
  }
</script>
<template>
  <!-- <div>
    <h2>Student Registration Form</h2>
    <input v-model="studentName" placeholder="Enter student name" />
     
    <p>Student Name: {{ studentName }}</p>
  </div> -->
  <!-- <form @submit.prevent="submitForm">
    <label>Name: </label>
    <input v-model="name" type= "text"/>
    <button type="submit">Register</button>
    
    <p>Message: {{ message }}</p>
  </form> -->
  <!-- <form @submit.prevent="register">
    <input v-model="name" placeholder="Enter your name"/>
    <input v-model="email" text="email" placeholder="Enter your email" required/>
    <button type="submit">Submit</button>
  </form> -->
  <!-- <textarea v-model="message"></textarea>
  <p>Message: {{ message }}</p> -->
  <!-- <p>Email: {{ email }}</p> -->
   <!-- <input type="radio" value="Yes" v-model="acceptedTerms" />
   <input type="radio" value="No" v-model="acceptedTerms" />
   <p>{{  acceptedTerms }}</p> -->
   <!-- <select v-model="course">
    <option>BSIT</option>
    <option>BSIS</option>
    <option>BSCS</option>
  </select>
  <p>{{ course }}</p> -->
  <!-- <h2>{{  studentName }}</h2> -->
   <!-- <button @click="saveStudentName">Save</button> -->
    <button @click="submitStudent">Submit</button>
</template>