<script setup>
// Nenhum import ou props necessários agora
</script>

<template>
  <section class="section_cards">
    <div class="section_head">
      <h2>Por que escolher a Nolasco Body Face?</h2>
      <p>Conheça nossos diferenciais</p>
    </div>

    <div class="cards_grid">
      <div class="card">
        <img src="../assets/images/logo.png" alt="Logo" class="logo" />
        <div class="content">
          <h3>Carinho</h3>
          <p>Todos nossos clientes recebem o melhor tratamento.</p>
        </div>
      </div>

      <div class="card">
        <img src="../assets/images/logo.png" alt="Logo" class="logo" />
        <div class="content">
          <h3>Profissionalismo</h3>
          <p>Nossa equipe é altamente qualificada e experiente.</p>
        </div>
      </div>

      <div class="card">
        <img src="../assets/images/logo.png" alt="Logo" class="logo" />
        <div class="content">
          <h3>Tecnologia</h3>
          <p>Utilizamos equipamentos de última geração para garantir os melhores resultados.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  padding: 2rem 1rem 4rem 1rem;
  background-color: var(--timberwolf);
}

/* Cabeçalho da seção */
.section_head {
  text-align: center;
  color: var(--bronze);
}

.section_head h2 {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
}

.section_head p {
  font-size: 1.2rem;
}

/* Grid dos cards */
.cards_grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 2rem;
  margin-top: 3rem;
  justify-items: center;
}

/* Card */
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
  align-items: center;
  justify-content: center;
}

/* Logo no canto superior esquerdo */
.card .logo {
  position: absolute;
  top: -15px;
  left: -50px;
  rotate: -15deg;
  width: 80%;
  opacity: 0.9;
  z-index: 1;
}

/* Conteúdo */
.card .content {
  position: relative;
  z-index: 2;
  text-align: center;
  padding: 0 0.5rem;
}

.card h3 {
  font-size: 1.8rem;
  font-weight: 600;
  margin-bottom: 10px;
}

.card p {
  font-size: 0.95rem;
}

/* Deixe os cards responsivos para mobile e para tablet */
@media (max-width: 600px) {
  .card {
    width: 90%;
    height: auto;
    padding: 2rem 1rem;
  }
}
</style>
