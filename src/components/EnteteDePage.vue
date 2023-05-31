<script setup>

</script>

<template>
  <header>
    <!-- Logo du site -->
    <router-link to="/">
      <img src="img/logo-jppjsl.png"
           class="logo"
           alt="Logo de J&#039;peux pas j&#039;ai sabre laser"
      >
    </router-link>
    <nav>
    <ul>
      <li>
        <router-link to="/sabre" exact-active-class="actif">Nos sabres</router-link>
      </li>
      <li>
        <router-link to="/service-client" exact-active-class="actif">Service client</router-link>
      </li>
    </ul>
  </nav>
  </header>
</template>

<style scoped>

</style>