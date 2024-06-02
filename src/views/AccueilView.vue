<script setup>
const tableauSabres = [
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
      <div v-for="unSabre in tableauSabres" :key="unSabre.id" class="sabre">
        <RouterLink :to="'/sabre/' + unSabre.id">
          <figure>
            <img :src="'/img/' + unSabre.image" :alt="unSabre.nom">
            <figcaption>
              <h2>{{ unSabre.nom }}</h2>
              <div class="prix">{{unSabre.prix}} CHF</div>
            </figcaption>
          </figure>
        </RouterLink>
      </div>
      <div class="sabre rupture">
        <a href="sabre.html">
          <figure>
            <img src="/img/sl-cal.jpg" alt="Sabre laser Cal Kestis">
            <figcaption>
              <p>Noooon, les stocks sont vides !</p>
              <h2>Sabre laser Cal Kestis</h2>
              <div class="prix">349 CHF</div>
            </figcaption>
          </figure>
        </a>
      </div>
    </div>
  </main>
</template>

<style scoped>

/********** STYLE PAGE ACCUEIL *********/
.page-accueil .sabres {
  display: flex;
  flex-wrap: wrap;
  gap: 1.25rem;
  align-content: space-evenly;
  justify-content: center;
  padding: 0;
}

.page-accueil .sabres .sabre {
  overflow: hidden;
  flex: 2 0 300px;
  padding: 0;
  border-radius: 10px;
  box-shadow: 0 0.03rem 0.06rem rgba(0, 0, 0, 0.2), 0 0.1rem 0.3rem rgba(0, 0, 0, 0.2);
  margin-bottom: 2rem;
  transition: all 0.3s ease-in-out;
  cursor: pointer;
  background-color: #e72854;
}

.page-accueil .sabres .sabre:hover {
  box-shadow: 0 0.03rem 0.06rem rgba(0, 0, 0, 0.6), 0 0.1rem 0.3rem rgba(0, 0, 0, 0.6);
  background-color: #6bbbda;
}

.page-accueil .sabres .sabre.rupture {
  background-color: #27282a;
}

.page-accueil .sabres .sabre figure {
  padding: 0;
  margin: 0;
}

.page-accueil .sabres .sabre figcaption {
  padding: 1rem;
  color: white;
}

</style>