<script setup>
import { ref } from 'vue'
const emoji = ref('🚀')
</script>

<template>
  <header class="header">
    <div>
      <img src="/src/assets/images/logo.png" />
    </div>
    <nav>
      <ul>
        <li><a href="#hero">Home</a></li>
        <li><a href="promos">Promoções</a></li>
        <li><a href="about">Sobre</a></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.header {
  background-color: var(--eerie-black);
  padding: 0 2rem;
  color: var(--bronze);
  display: flex;
  justify-content: space-around;
  align-items: center;
}

img {
  height: 100px;
  width: auto;
}

ul {
  list-style: none;
  display: flex;
  justify-content: right;
  gap: 2rem;
  margin: 0;
  padding: 0;
}

a {
  color: var(--bronze);
  text-decoration: none;
  font-weight: bold;
  font-size: 1.2rem;
}
</style>
