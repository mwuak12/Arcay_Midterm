<script setup>
import { ref, computed } from 'vue'

const course = ref("Web Systems")
const instructor = ref("Mr. Ampong")
const room = ref("Lab 2")

const quizScore = ref(18)
const perfectScore = ref(20)
const percentage = computed(() => {
  return (quizScore.value / perfectScore.value) * 100
})
const score = ref(0)
const classStatus = ref("Closed")
function toggleStatus() {
  classStatus.value = classStatus.value === "Closed" ? "Open" : "Closed"
}
const logo = "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTOc3nO-BaAtplLZ2Zcn-C7S0zTNsJXu9baSlk3r6_xZw&s=10"

const portal = "https://sis.materdeicollege.com/"
</script>
<template>
  <div>
    <h1>Course Information</h1>

    <h2>Task 1</h2>
    <p><strong>Course:</strong> {{ course }}</p>
    <p><strong>Instructor:</strong> {{ instructor }}</p>
    <p><strong>Room:</strong> {{ room }}</p>
    <hr>

  
    <h2>Task 2</h2>
    <p>Quiz Score: {{ quizScore }}</p>
    <p>Perfect Score: {{ perfectScore }}</p>
    <p><strong>Percentage: {{ percentage }}%</strong></p>
    <hr>
   
    <h2>Task 3</h2>
    <p>Score: {{ score }}</p>
    <button @click="score++">Add Point</button>
    <hr>

  
    <h2>Task 4</h2>
    <p>Class Status: {{ classStatus }}</p>
    <button @click="toggleStatus">Change Status</button>
    <hr>

  
    <h2>Task 5</h2>
    <img :src="logo" alt="School Logo" width="150">
    <hr>


    <h2>Task 6</h2>
    <a :href="portal" target="_blank">Visit School Portal</a>
    <hr>

  
    <h2>Task 7</h2>
    <button :disabled="true">Enroll</button>
  </div>

</template>

<style>
button {
  margin-top: 10px;
  padding: 8px 15px;
}
</style>