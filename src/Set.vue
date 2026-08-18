<script setup>
import { ref ,computed} from 'vue';
const name = ref(['Alex','Ben','Carla','Daina'])
const showProfile = ref(false)
const score = 80
const subject = ref(['Math','English','Science'])
const totalSubject = computed(() => {
    return subject.value.length
 })
</script>

<template>
    <h2>1.</h2>
<div>
    <ul>
        <li v-for = "names in name" :key = "names">
            {{ names }}
        </li >
    </ul>
    </div>
    <h2>2.</h2>
     <div v-show="showProfile">Student Profile</div>
    <h2>3.</h2>
     <h2 v-if="score >= 90">Excellent</h2>
     <h2 v-else-if="score >= 75">Passed</h2>
     <h2 v-else="score">Failed</h2>
     <h2>4.</h2>
     <div>Total Subjects: {{ totalSubject }}</div>
</template>