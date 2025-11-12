<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
</script>

<template>
  <header class="header">
    <div class="logo">
      <img src="/src/assets/images/logo.png" alt="Logo" />
    </div>

    <button class="menu-toggle" @click="toggleMenu" aria-label="Abrir menu">
      <span :class="{ open: isMenuOpen }"></span>
      <span :class="{ open: isMenuOpen }"></span>
      <span :class="{ open: isMenuOpen }"></span>
    </button>

    <nav :class="{ open: isMenuOpen }">
      <ul>
        <li><a href="#hero" @click="isMenuOpen = false">Home</a></li>
        <li><a href="#promos" @click="isMenuOpen = false">Promoções</a></li>
        <li><a href="#about" @click="isMenuOpen = false">Sobre</a></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.header {
  background-color: var(--eerie-black);
  padding: 0.5rem 2rem;
  color: var(--bronze);
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: relative;
  z-index: 10;
}

.logo img {
  height: 80px;
  width: auto;
}

/* Menu padrão (desktop) */
nav ul {
  list-style: none;
  display: flex;
  gap: 2rem;
  margin: 0;
  padding: 0;
}

a {
  color: var(--bronze);
  text-decoration: none;
  font-weight: bold;
  font-size: 1.1rem;
}

a:hover {
  opacity: 0.8;
}

/* Botão hamburguer (escondido no desktop) */
.menu-toggle {
  display: none;
  flex-direction: column;
  justify-content: space-between;
  width: 28px;
  height: 20px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
  z-index: 20;
}

.menu-toggle span {
  display: block;
  height: 3px;
  width: 100%;
  background-color: var(--bronze);
  border-radius: 3px;
  transition: 0.3s;
}

/* Efeitos de abertura do menu hamburguer */
.menu-toggle span.open:nth-child(1) {
  transform: translateY(8px) rotate(45deg);
}
.menu-toggle span.open:nth-child(2) {
  opacity: 0;
}
.menu-toggle span.open:nth-child(3) {
  transform: translateY(-8px) rotate(-45deg);
}

/* Responsividade */
@media (max-width: 768px) {
  nav {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background-color: var(--eerie-black);
    overflow: hidden;
    max-height: 0;
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease-in-out;
  }

  .header {
    justify-content: space-between;
  }

  /* Quando o menu abre */
  nav.open {
    max-height: 300px; /* aumenta para garantir espaço suficiente */
    opacity: 1;
    visibility: visible;
  }

  nav ul {
    flex-direction: column;
    align-items: center;
    padding: 1rem 0;
    gap: 1rem;
  }

  .menu-toggle {
    display: flex;
  }
}
</style>
