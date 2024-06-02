<script setup>

</script>

<template>
  <main class="page-accueil">
    <h1>Découvrez nos sabres <strong>LASER</strong></h1>

    <div class="sabres">
      <div class="sabre">
        <RouterLink to="/sabre/:id">
          <figure>
            <img src="/img/sl-cal.jpg" alt="Sabre laser Cal Kestis">
            <figcaption>
              <h2>Sabre laser Cal Kestis</h2>
              <div class="prix">349 CHF</div>
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