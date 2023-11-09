<template>
    <div>
        <h2>votre email:{{ user.email }}
        </h2>
        <h2>votre adresse:{{ user.adresse }}
        </h2>
    </div>
</template>

<script setup>
import { ref } from 'vue';
const user = ref({ email: 'iit@gmail.com', adresse: "cité ons" })

</script>

<style lang="scss" scoped>
h1 {
    color: blue($color: blue);
    font-size: 30px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;

}
</style>