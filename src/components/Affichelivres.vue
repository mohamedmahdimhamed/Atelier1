<template>
  <div v-for="liv in props.livres" :key="liv.isbn">
    <div class="card" style="width: 22rem">
      <img :src="liv.couverture" class="card-img-top" height="120" width="auto"/>
      <div class="card-body">
        <h5 class="card-title">Auteur: {{ liv.auteur }}</h5>
        <h5 class="card-text">Titre de livre: {{ liv.titre }}</h5>
        <h5 class="card-text">Prix: {{ liv.Prix }} DT</h5>
        <a href="#" class="btn btn-primary">Add to card</a>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(["livres"]);
</script>

<style lang="scss" scoped>
</style>