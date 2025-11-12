<script setup></script>

<template>
  <section class="banner">
    <div class="banner-scroll">
      <!-- Conteúdo original -->
      <div class="banner-content">
        <img src="../assets/images/logo-icone.png" alt="logo-icone da faixa" />
        <span>AINDA DÁ TEMPO – MELHORE SUA AUTOESTIMA</span>
        <img src="../assets/images/logo-icone.png" alt="logo-icone da faixa" />
        <span>UMA VIDA EXTRAORDINÁRIA TE ESPERA</span>
        <img src="../assets/images/logo-icone.png" alt="logo-icone da faixa" />
        <span>SINTA-SE BEM CONSIGO MESMO </span>
        <img src="../assets/images/logo-icone.png" alt="logo-icone da faixa" />
        <span>MARQUE JÁ SUA CONSULTA -- NÃO PERCA TEMPO</span>
      </div>

      <!-- Cópia idêntica (para o looping) -->
      <div class="banner-content">
        <img src="../assets/images/logo-icone.png" alt="logo-icone da faixa" />
        <span>AINDA DÁ TEMPO – MELHORE SUA AUTOESTIMA</span>
        <img src="../assets/images/logo-icone.png" alt="logo-icone da faixa" />
        <span>UMA VIDA EXTRAORDINÁRIA TE ESPERA</span>
        <img src="../assets/images/logo-icone.png" alt="logo-icone da faixa" />
        <span>SINTA-SE BEM COM SI PRÓPRIO - MARQUE JÁ SUA CONSULTA</span>
        <img src="../assets/images/logo-icone.png" alt="logo-icone da faixa" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.banner {
  overflow: hidden;
  background: linear-gradient(to right, #b38b5a, #1d1d1a);
  padding: 10px 0;
  white-space: nowrap;
}

.banner-scroll {
  display: flex;
  width: max-content;
  animation: scroll 45s linear infinite;
}

.banner-content {
  display: flex;
  align-items: center;
  gap: 2rem;
}

.banner-content img {
  height: 60px;
  width: auto;
}

.banner-content span {
  color: var(--timberwolf);
  font-weight: 600;
  font-size: 14px;
  text-transform: uppercase;
}

/* Animação contínua */
@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}
</style>
