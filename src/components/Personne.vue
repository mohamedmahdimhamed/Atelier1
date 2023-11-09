
<script setup>
import { ref } from 'vue';
const nom = ref('Mohamed');
const age = ref(18);
</script>
<template>
    <h2>Je m'appelle {{ nom }}</h2><br>
    <p class="item">J'ai {{ age }}</p>
</template>
<style scoped>
h1 {
    color: red;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    font-size: xx-large;
}

.item {
    color: darkmagenta;
    font-size: small;
}</style>