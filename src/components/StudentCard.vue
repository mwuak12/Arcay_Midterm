<script setup>
defineProps({
    name: String,
    isPassed: Boolean
})
</script>

<template>     
        <p :class="{pass: isPassed}">{{ name }}</p>  
</template>

<style>
.pass{
  color : green;
  font-weight: bold;
}
</style>