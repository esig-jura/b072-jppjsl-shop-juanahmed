<script setup>

import {RouterLink} from "vue-router";
</script>

<template>
  <header>
    <RouterLink to="/">
      <img src="/img/logo-jppjsl.png"
           class="logo"
           alt="Logo de J&#039;peux pas j&#039;ai sabre laser"
      >
    </RouterLink>
    <nav>
      <ul>
        <li><RouterLink active-class="actif" to="/">Home</RouterLink></li>
        <li><RouterLink active-class="actif" to="/service-client">Service client</RouterLink></li>
        <li><RouterLink active-class="actif" to="/sabre/:id">Fiche du sabre 1</RouterLink></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>

/********** STYLE HEADER *********/
header {
  background-color: #eeeeee;
  padding: 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  gap: 20px;
}

header .logo {
  max-height: 150px;
}

/********** STYLE NAVIGATION *********/

header nav ul {
  display: flex;
  padding: 0;
  margin: 0;
  list-style: none;
  margin-left: auto;
}

header nav a {
  font-size: 1.25rem;
  padding: 1em;
  font-weight: bold;
  color: #3b3d40;
}

header nav a.actif {
  color: #6bbbda;
}

header nav a:hover {
  color: #e72854;
}

</style>