<script setup>
import { defineProps } from 'vue'
const props = defineProps({
  cardTitle: {
    type: String,
    required: true,
  },
  cardText: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="card">
    <img src="../assets/images/logo.png" alt="Logo Nolasco Bodyface" class="logo" />
    <div class="content">
      <h3>{{ cardTitle }}</h3>
      <p>{{ cardText }}</p>
    </div>
  </div>
</template>

<style scoped>
:root {
  --silver: #c0c0c0ff;
  --timberwolf: #d9dbd3ff;
}

.card {
  position: relative;
  width: 300px;
  height: 300px;
  border-radius: 12px;
  overflow: hidden;
  background: linear-gradient(135deg, var(--bronze), var(--eerie-black));
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  color: var(--timberwolf);
  display: flex;
}

/* Logo no canto superior esquerdo */
.card .logo {
  position: absolute;
  top: -15px;
  left: -50px;
  rotate: -15deg;
  width: 80%;
  height: auto;
  z-index: 1;
  opacity: 0.9;
}

/* Conteúdo do card */
.card .content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0 0.2rem;

  position: relative;
  z-index: 2; /* Garante que o texto fique sempre na frente */
  text-align: center;
}

.card h3 {
  font-size: 1.8rem;
  font-weight: 600;
  margin-bottom: 10px;
}

.card p {
  font-size: 0.95rem;
  color: var(--timberwolf);
}
</style>
