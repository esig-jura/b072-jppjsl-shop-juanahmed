<script setup>

import {RouterLink} from "vue-router";

const props = defineProps({
  sabre: {
    type: Object,
    required: true,
  }
})

</script>

<template>
  <div class="sabre">
    <RouterLink :to="'/sabre/' + unSabre.id">
      <figure>
        <img :src="'/img/' + unSabre.image" :alt="unSabre.nom">
        <figcaption>
          <h2>{{ unSabre.nom }}</h2>
          <div class="prix">{{ unSabre.prix }} CHF</div>
        </figcaption>
      </figure>
    </RouterLink>
  </div>
</template>

<style scoped>

</style>