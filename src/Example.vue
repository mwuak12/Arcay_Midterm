<script setup>
// import {ref} from 'vue'
// import {ref, computed} from 'vue'
// const students = ref(['Matt','John','Peter','Jack'])
// const student = ref([
//     {id: 1, name: 'John', age: 20},
//     {id: 2, name: 'Ampong', age: 22},
//     {id: 3, name: 'Jack', age: 24},
//     {id: 4, name: 'Jon', age: 25}
    
// ])
// const isLoggedIn = ref(true)
// const score = ref(85)
// const firstName = ref('John')
// const lastName = ref('Aplacador')
// const fullName = computed(() => {
//     return firstName.value + ' ' + lastName.value
// })
// const students = ref(['John','Aw','Peter','Mark', 'Apla'])
// const totalstudents = computed(() => {
//     return students.value.length
// })
// const filteredStudent = computed(() => students.value.filter(student => student.startsWith('M')))
// const students = ref([
//     {id: 1, name: 'Alice', passed: true},
//     {id: 2, name: 'Rrr', passed: false},
//     {id: 3, name: 'Pee', passed: true}
// ])
// const passedStudents = computed(() => {
//     return students.value.filter(student => student.passed)
// })
</script>
<template>
    <!-- <div v-for = "item in student" :key = "item.id">
        {{ item.name }} - {{ item.age }}
    </div>
    <ul>
        <li v-for = "student in students" :key = "student">
            {{ student }}
        </li>
    </ul>
    <li v-for = "(student, index) in student" :key = "student.id">
            {{ index + 1 }} . {{ student.name }}
        </li> -->
        <!-- <h2 v-if="isLoggedIn">Welcome Back!</h2>
        <h2 v-else>Please Login!</h2> -->
        <!-- <h2 v-if="score >= 90">Excellent</h2>
        <h2 v-else-if="score >= 75">Passed</h2>
        <h2 v-else="score">Failed</h2> -->
        <!-- <h2 v-show="isLoggedIn">Welcome!!</h2> -->
        <!-- {{ fullName }} -->
        <!-- <h2>Total Students: {{ totalstudents }}</h2> -->
        <!-- <li v-for="student in filteredStudent" :key="student">
            <ul>{{ student }}</ul>
        </li> -->
        <!-- <div v-for="student in passedStudents" :key="student.id">
            <p v-if="student.passed">
                {{ student.name }} - Passed
            </p>
        </div> -->
</template>