<script setup>
import { ref } from 'vue'
const header_message = ref('Realce sua beleza com tecnologia e cuidado personalizado')
const message = ref(
  'Na Nolasco Body Face, unimos inovação e expertise em estética facial e corporal para oferecer resultados visíveis, seguros e feitos sob medida para você.',
)
</script>

<template>
  <section class="hero">
    <img
      src="../assets/images/dra/NolascoHair_DraGilmara_DrPaulo_2025JUL-011.png"
      alt="foto da Dra. Gilmara com o Dr. Paulo"
    />
    <div class="hero_text">
      <h1>{{ header_message }}</h1>
      <p>{{ message }}</p>
    </div>
  </section>
</template>

<style scoped>
.hero {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-evenly;
  padding: 0 2rem;
  background-color: var(--eerie-black);
  mask-image: linear-gradient(to bottom, black 80%, transparent 100%);
}
.hero img {
  width: 480px;
  height: auto;
  border-radius: 10px;
  margin-right: 2rem;
}
.hero_text {
  color: var(--bronze);
  max-width: 600px;
}
.hero_text h2 {
  margin-bottom: 1rem;
}
.hero_text p {
  font-size: 1.2rem;
}
</style>
