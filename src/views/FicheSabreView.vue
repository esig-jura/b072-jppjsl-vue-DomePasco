<script setup>
import {useSabresStore} from "@/stores/sabres";

// Définition des propriétés du composant
const props = defineProps(['id'])

//récupération magasin des sabres
const storeSabres = useSabresStore()

//récupère le tableau des sabres du magasin par ordre alphabétique
const sabre = storeSabres.getSabreById(props.id)

</script>

<template>
  <main class="page-sabre">
    <div class="sabre">
      <h1>{{ sabre.nom}}</h1>

      <img :src="'/img/' + sabre.image" :alt="sabre.nom">
      <!-- ou bien méthode 2 : <img :src="`/img/${sabre.image}`" :alt="sabre.nom"> -->

      <p>{{ sabre.description }}</p>

      <ul class="details">
        <li>Prix: {{ sabre.prix }} CHF</li>
        <li>Stock: {{ sabre.stock }} pièces</li>
        <li>Longueur: {{ sabre.longueur }}cm</li>
        <li>Poids: {{ sabre.poids }} kg</li>
      </ul>
    </div>
  </main>
</template>

