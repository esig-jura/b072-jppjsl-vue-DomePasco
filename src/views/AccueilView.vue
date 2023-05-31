<script setup>
import SabreLaser from "@/components/SabreLaser.vue";
import {useSabresStore} from "@/stores/sabres";

//récupération magasin des sabres
const storeSabres = useSabresStore()

//récupère le tableau des sabres du magasin par ordre alphabétique
const sabres = storeSabres.getSabresAZ

</script>
<template>
  <main class="page-accueil">
    <h1>Découvrez nos sabres <strong>LASER</strong></h1>

    <ul class="sabres">
      <SabreLaser
        v-for="sabre in sabres"
        :key="sabre.id"
        :sabre="sabre"
      />
    </ul>
  </main>
</template>

