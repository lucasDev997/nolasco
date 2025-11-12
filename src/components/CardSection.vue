<script setup>
import Card from '@/components/Card.vue'
</script>

<template>
  <section>
    <div class="section_head">
      <h2>Nossos Diferenciais</h2>
      <p>Conheça os motivos que fazem da Nolasco Bodyface a escolha certa para você.</p>
    </div>
    <div class="section_cards">
      <Card
        cardTitle="Carinho"
        cardText="Todos nossos clientes recebem o melhor tratamento."
      ></Card>
      <Card
        cardTitle="Profissionalismo"
        cardText="Nossa equipe é altamente qualificada e experiente."
      ></Card>
      <Card
        cardTitle="Tecnologia"
        cardText="Utilizamos equipamentos de última geração para garantir os melhores resultados."
      ></Card>
    </div>
  </section>
</template>

<style scoped>
div.section_head {
  text-align: center;
  color: var(--bronze);
}
div.section_head h2 {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
}
div.section_head p {
  font-size: 1.2rem;
}
div.section_cards {
  display: flex;
  justify-content: space-evenly;
}
section {
  padding: 2rem 0 4rem 2rem;
  background-color: var(--timberwolf);
}
</style>
