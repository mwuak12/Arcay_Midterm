<script setup>
import { ref } from 'vue'   
import { defineEmits } from 'vue'

const emit = defineEmits(['submitStudent'])

const studentName = ref('')
const studentID = ref('')
const email = ref('')
const bookCategory = ref('')
const requestType = ref('')
const confirmation = ref(false)
const reason = ref('')


const accept = ref('')


function submitForm() {
  emit('submitStudent', {
    name: studentName.value,
    id: studentID.value,
    email: email.value,
    bookCategory: bookCategory.value,
    requestType: requestType.value,
    reason: reason.value
  })
}


</script>
<template>

<form @submit.prevent="OnChange">

    <label for="studentName">Student Name:</label>
    <input v-model="studentName" type="text" id="studentName" required>
    <label for="studentID">Student ID:</label>
    <input v-model="studentID"type="text" id="studentID" required>

    <label for="email">Email:</label>
    <input v-model="email" type="email" id="email" required>
 
    <label>Book Category:</label>
    <select v-model="bookCategory">
      <option>Programming</option>
      <option>Web Development</option>
      <option>Database</option>
      <option>Networking</option>
      <option>Software Engineering</option>
    </select>
     <input type="radio" value="Yes" />
   <input type="radio" value="No"/>
   
    <label>Request Type:</label>
    <select v-model="requestType">
      <option>Borrow</option>
      <option>Reserve</option>
      <option>Reference</option>
    </select>
    <label>
    <input id ="ap" v-model="accept" type="checkbox" required>
    I agree
    </label>
  
    <label>Reason for Reservation:</label>
    <textarea v-model="reason"></textarea>
    


  <button @click="submitForm">Submit Request</button>

 
  <div>
    <p>Student Name: {{ studentName }}</p>
    <p>Student ID: {{ studentID }}</p>
    <p>Email: {{ email }}</p>
    <p>Book Category: {{ bookCategory }}</p>
    <p>Accepted Terms: {{ accept }}</p>
    <p>Reason for Reservation: {{ reason }}</p>
    <p>Request Type: {{ requestType }}</p>
    
  </div>
</form>
</template>



