<script setup>




</script>

<template>
  <main class="page-sabre">
    <div class="sabre">
      <h1>Sabre laser Cal Kestis</h1>

      <img src="/img/sl-cal.jpg" alt="Sabre laser Cal Kestis">

      <p>
        Le SL-Cal est un sabre laser de la gamme REPLIKA.
        Inspiré par le sabre de Cal Kestis, dans le jeu
        « Fallen Order » (réplique non officielle).
      </p>

      <ul class="details">
        <li>Prix: 349 CHF</li>
        <li>Stock: plus de 10 pièces</li>
        <li>Longueur: 38cm</li>
        <li>Poids: 0,600 kg</li>
      </ul>
    </div>
  </main>
</template>

<style scoped>

/********** STYLE PAGE SABRE *********/
.page-sabre .sabre {
  max-width: 500px;
  margin: 0 auto;
}

.page-sabre .sabre img {
  border: 6px solid #e72854;
}

.page-sabre ul.details {
  list-style-type: none;
  padding: 0;
  margin: 1rem 0;
  font-size: 1.1rem;
}

.page-sabre ul.details li {
  padding: .5em 1em;
}

.page-sabre ul.details li:nth-child(odd) {
  background-color: #eeeeee;
}

</style>