<script setup>
import { ref } from 'vue'

const header_message = ref('Realce sua beleza com tecnologia e cuidado personalizado')
const message = ref(
  'Na Nolasco Body Face, unimos inovação e expertise em estética facial e corporal para oferecer resultados visíveis, seguros e feitos sob medida para você.',
)
</script>

<template>
  <section class="hero">
    <div class="hero_image">
      <img
        src="../assets/images/dra/NolascoHair_DraGilmara_DrPaulo_2025JUL-011.png"
        alt="foto da Dra. Gilmara com o Dr. Paulo"
      />
    </div>

    <div class="hero_text">
      <h1>{{ header_message }}</h1>
      <p>{{ message }}</p>
    </div>
  </section>
</template>

<style scoped>
.hero {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 80vh;
  overflow: hidden;
}

.hero_image img {
  position: relative;
  inset: 0;
  width: 100%;
  object-fit: cover;
  height: 1000px;
  width: auto;
  mask-image: linear-gradient(to bottom, black 80%, transparent 100%);
  -webkit-mask-image: linear-gradient(to bottom, black 80%, transparent 100%);
}

.hero_text {
  position: relative;
  z-index: 2;
  color: var(--bronze);
  text-align: center;
  max-width: 600px;
  padding: 2rem;
  background: rgba(29, 29, 26, 0.6); /* leve overlay */
  border-radius: 12px;
}

.hero_image img:hover {
  transform: scale(1.03);
}

.hero_text h1 {
  font-size: 2rem;
  margin-bottom: 1rem;
}

.hero_text p {
  font-size: 1.2rem;
  line-height: 1.6;
}

/* ===== Responsividade ===== */

/* Tablets (até 1024px) */
@media (max-width: 1024px) {
  .hero {
    flex-direction: column;
    text-align: center;
    padding: 2rem 1.5rem;
  }

  .hero_image {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .hero_image img {
    height: 800px;
    width: auto;
    mask-image: linear-gradient(to bottom, var(--eerie-black) 85%, transparent 100%);
  }

  .hero_text {
    max-width: 90%;
  }

  .hero_text h1 {
    font-size: 1.8rem;
  }

  .hero_text p {
    font-size: 1.1rem;
  }
}

/* Celulares (até 600px) */
@media (max-width: 600px) {
  .hero {
    padding: 1.5rem 1rem;
    mask-image: linear-gradient(to bottom, var(--eerie-black) 85%, transparent 100%);
    position: relative;
  }

  .hero_text {
    position: absolute;
    top: 50%;
  }

  .hero_image {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .hero_image img {
    height: 700px;
    width: auto;
    mask-image: linear-gradient(to bottom, var(--eerie-black) 75%, transparent 100%);
  }

  .hero_text h1 {
    font-size: 1.5rem;
  }

  .hero_text p {
    font-size: 1rem;
  }
}
</style>
