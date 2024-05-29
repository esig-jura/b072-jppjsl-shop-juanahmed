<script setup>
import { RouterView } from 'vue-router'
import EnteteDePage from "@/components/EnteteDePage.vue";
import PiedDePage from "@/components/PiedDePage.vue";
</script>

<template>
  <EnteteDePage/>
  <main>
    <RouterView />
  </main>
  <PiedDePage/>
</template>

<style scoped>

</style>