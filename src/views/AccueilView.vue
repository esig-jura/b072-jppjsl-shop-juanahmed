<script setup>

import {RouterLink} from "vue-router";

const sabres = [
    {
      id: 445,
      nom: 'SL-VAD',
      image: 'sl-vad.jpg',
      stock: 4,
      prix: 399,
      poids: 1.5,
      longueur: 28,
      description:
          'Le SL-VAD est un sabre laser de la gamme REPLIKA. Inspiré' +
          ' par le sabre du méchant le plus iconique du cinéma, Dark Vador,' +
          'tel qu’on peut le voir dans la saga Star Wars, version Empire,' +
          'Episode IV, IV et VI. (réplique non officielle).'
    },
    {
      id: 4,
      nom: 'SL-SKY',
      image: 'sl-sky.jpg',
      stock: 0,
      prix: 399,
      poids: 0.999,
      longueur: 28,
      description:
          'Le SL-Sky (V2) est le premier sabre de la gamme REPLIKA.' +
          ' Inspiré par le sabre de Luke Skywalker, version « Retour du Jedi ».' +
          ' (réplique non officielle).'
    },
    {
      id: 67,
      nom: 'SL-OBI 1',
      image: 'sl-obi.jpg',
      stock: 22,
      prix: 379,
      poids: 1.5,
      longueur: 28.5,
      description:
          'Le SL-OBI 1 est une de nos dernières sorties sabre de la gamme' +
          'REPLIKA. Inspiré par le sabre de Obi-wan Kenobi version Episode I ' +
          '(réplique non officielle).'
    },
    {
      id: 99,
      nom: 'SL-CAL',
      image: 'sl-vad.jpg',
      stock: 8,
      prix: 399,
      poids: 0.6,
      longueur: 38,
      description:
          'Le SL-Cal est un sabre laser de la gamme REPLIKA.' +
          'Inspiré par le sabre de Cal Kestis,' +
          'dans le jeu « Fallen Order » (réplique non officielle).'
    },
    {
      id: 111,
      nom: 'SL-TANO-curve',
      image: 'sl-tano-curve.jpg',
      stock: 15,
      prix: 699,
      poids: 0.6,
      longueur: 27.5,
      description:
          'Les SL-TANO Curve sont deux de nos dernières sorties sabre de' +
          'la gamme REPLIKA. Inspirés par les doubles sabres d’Ashoka' +
          'Tano version Mandalorian (réplique non officielle).'
    },
    {
      id: 345,
      nom: 'SL-PIKE',
      image: 'sl-pike.jpg',
      stock: 2,
      prix: 189,
      poids: 1.9,
      longueur: 69,
      description:
          'La SL-PIKE est notre modèle de lance laser de référence ! ' +
          'Idéal pour compléter un cosplay, étudié pour le combat.'
    },
    {
      id: 373,
      nom: 'SL-Opress',
      image: 'sl-opress.jpg',
      stock: 6,
      prix: 499,
      poids: 1.5,
      longueur: 65,
      description:
          'La SL-PIKE est notre modèle de lance laser de référence ! ' +
          'Idéal pour compléter un cosplay, étudié pour le combat.'
    }
]


</script>

<template>
  <main class="page-accueil">
    <h1>Découvrez nos sabres <strong>LASER</strong></h1>

    <div class="sabres">
      <div class="sabre" v-for="sabre in sabres">
        <RouterLink class="actif" to="/sabre/1">
          <figure>
            <img :src="'/img/' + sabre.image" alt="Sabre laser Cal Kestis">
            <figcaption>
              <h2>Sabre laser Cal Kestis</h2>
              <div class="prix">349 CHF</div>
            </figcaption>
          </figure>
        </RouterLink>
      </div>
      <div class="sabre rupture">
        <RouterLink class="actif" to="/sabre/1">
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