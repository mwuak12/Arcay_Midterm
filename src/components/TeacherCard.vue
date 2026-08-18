<script setup>
defineProps({
    name : String,
    subject : String,
    adviser : Boolean

})
</script>

<template>
    <p :class ="{colors : adviser}">{{ name }}</p>
    <p :class ="{colors : adviser}">{{ subject }}</p>
</template>
<style>
    .colors{
        color : rgb(55, 0, 255);
        font-weight: bold;
    }
</style>