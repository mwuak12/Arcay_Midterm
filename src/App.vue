<script setup>

// import HelloWorld from './components/HelloWorld.vue'
// import SampleCom from './components/SampleCom.vue';
// import StudentCard from './components/StudentCard.vue';
// import Header from './components/Header.vue';
// import Footer from './components/Footer.vue';
// import Book from './components/Book.vue';
// const  isActive = true
// import TeacherCard from './components/TeacherCard.vue';
// import Studentcard from './components/Studentcard.vue';
// import FormActivity from './components/FormActivity.vue';
import BookRequestForm from './components/BookRequestForm.vue';
function receiveStudent(student) {
  console.log(student.name)
  console.log(student.id)
  console.log(student.email)
  console.log(student.bookCategory)
  console.log(student.requestType)
  console.log(student.reason)
  
  alert(`Student: ${student.name}, Student ID: ${student.id}`)
  alert(`Email: ${student.email}, Book Category: ${student.bookCategory}`)
  alert(`Request Type: ${student.requestType}, Reason: ${student.reason}`)

}
// function showMessage() {
//   alert("Student Saved !");
// }
// function receiveStudent(student) {
//   console.log(student.name)
//   console.log(student.age)
  
//   alert(`Student: ${student.name}, Age: ${student.age}`)
// }
</script>

<template>
  <!-- <HelloWorld /> -->
  <!-- <Header /> -->
  <!-- <StudentCard name = "Ampong" course = "BSIT"/> -->
  <!-- <Footer /> -->
   <!-- <div class ="active">
   <StudentCard name = "Aplacador" :isPassed= "true"/>
  <StudentCard name = "Ampong" :isPassed = "false"/> -->
   <!-- <p :class="{active: isActive}">Active Student</p> -->
    <!-- <Book BookName = "Harry Potter and the Sorcerers Stone" Author ="J. Roling" :isSold = "false"/>
    <Book BookName = "Harry Potter: The Goblet of Fire" Author="J. Roling" :isSold ="true"/>
    <Book BookName = "Harry Potter: Deathly Hollows" Author ="J. Roling" :isSold ="false"/> -->
<!-- </div> -->
 <!--<TeacherCard name = "Mr. Cruz" subject ="Programming" adviser ="true" />
 <TeacherCard name = "Mr. Reyes" subject ="Mathematics" adviser ="false" />
 <TeacherCard name = "Mr. Santos" subject ="Networking" adviser ="true" /> -->
 <!-- <Studentcard
 @save="showMessage"
 /> -->
 <!-- <FormActivity
 @submitStudent="receiveStudent"
 /> -->
 <BookRequestForm
 @submitStudent="receiveStudent"
 />
</template>

<!-- <style>
.active{
  color : green;
  font-weight: bold;
}
</style> -->
