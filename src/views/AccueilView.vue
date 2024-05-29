<script setup>

import {RouterLink} from "vue-router";

//const tableauSabres = [];

  // Import du magasin des sabres
  import { useSabresStore } from '@/stores/sabres'
  // Création d'une instance du magasin des sabres pour le composant
  const storeSabres = useSabresStore()
  // Récupération des données des sabres triés par ordre alphabétique
  const tableauSabres = storeSabres.getSabresAZ


</script>

<template>
  <main class="page-accueil">
    <h1>Découvrez nos sabres <strong>LASER</strong></h1>

    <div class="sabres">
      <div class="sabre" v-for="unSabre in tableauSabres" :key="unSabre.id">
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
      <div class="sabre rupture">
        <RouterLink class="actif" to="/sabre/2">
          <figure>
            <img src="/img/sl-cal.jpg" alt="Sabre laser Cal Kestis">
            <figcaption>
              <p>Noooon, les stocks sont vides !</p>
              <h2>Sabre laser Cal Kestis</h2>
              <div class="prix">349 CHF</div>
            </figcaption>
          </figure>
        </RouterLink>
      </div>
    </div>
  </main>
</template>

<style scoped>

</style>