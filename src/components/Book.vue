<script setup>
defineProps({
    BookName : String,
    Author : String,
    isSold : Boolean
})
</script>

<template>
        <h2 :class = "{pass : isSold}">Book: {{ BookName }}</h2>
        <p :class = "{pass : isSold}">Author: {{ Author }}</p>
</template>
<style>
.pass{
  color : rgb(128, 0, 0);
  font-weight: bold;
}
</style>