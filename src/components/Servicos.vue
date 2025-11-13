<template>
  <section class="servicos">
    <h2 class="titulo">Procedimentos</h2>

    <div class="cards-container">
      <transition-group name="slide" tag="div" class="cards-grid">
        <div class="card" v-for="(servico, index) in servicosVisiveis" :key="servico.nome">
          <h3>{{ servico.nome }}</h3>
          <p>{{ servico.descricao }}</p>
          <p class="preco">{{ servico.preco }}</p>
          <button class="btn">
            <a
              href="https://www.instagram.com/stories/highlights/17939012780848269/"
              target="_blank"
              >Saiba mais</a
            >
          </button>
        </div>
      </transition-group>
    </div>

    <div class="ver-mais-container">
      <button class="btn-toggle" @click="mostrarTodos = !mostrarTodos">
        {{ mostrarTodos ? 'Ver menos' : 'Ver todos' }}
      </button>
    </div>
  </section>
</template>

<script setup>
import { ref, computed } from 'vue'

const mostrarTodos = ref(false)

const servicos = [
  {
    nome: 'Toxina Botulínica - Terço Superior',
    descricao: 'Reduza rugas e linhas de expressão com resultados naturais.',
    preco: 'R$ 1.000,00',
  },
  {
    nome: 'Toxina Botulínica - Full Face',
    descricao: 'Tratamento completo para todo o rosto com harmonia e equilíbrio.',
    preco: 'R$ 2.000,00',
  },
  {
    nome: 'Preenchimento Labial - 1Ml',
    descricao: 'Realce o volume e formato dos lábios com naturalidade.',
    preco: 'R$ 1.200,00',
  },
  {
    nome: 'Preenchimento Rinomodelação',
    descricao: 'Melhore o formato nasal sem cirurgia.',
    preco: 'R$ 1.100,00',
  },
  {
    nome: 'Preenchimento Mento - 1Ml',
    descricao: 'Harmonize o perfil facial com definição sutil.',
    preco: 'R$ 1.000,00',
  },
  {
    nome: 'Preenchimento Mandíbula - 1Ml',
    descricao: 'Realce o contorno facial e traga definição ao rosto.',
    preco: 'R$ 1.000,00',
  },
  {
    nome: 'Preenchimento Olheira - 1Ml',
    descricao: 'Reduza olheiras e restaure o aspecto de descanso.',
    preco: 'R$ 1.000,00',
  },
  {
    nome: 'Preenchimento Malar - 1Ml',
    descricao: 'Devolva volume e firmeza à região das bochechas.',
    preco: 'R$ 1.000,00',
  },
  {
    nome: 'Preenchimento Bigode Chinês - 1Ml',
    descricao: 'Atenue linhas profundas ao redor da boca.',
    preco: 'R$ 1.000,00',
  },
  {
    nome: 'Bichectomia',
    descricao: 'Harmonize o formato do rosto com contornos mais definidos.',
    preco: 'R$ 1.500,00',
  },
  {
    nome: 'Lipoaspiração Cervical',
    descricao: 'Elimine o acúmulo de gordura abaixo do queixo.',
    preco: 'R$ 3.500,00',
  },
  {
    nome: 'Sculptra - 1 Sessão',
    descricao: 'Estimule o colágeno e mantenha a firmeza da pele.',
    preco: 'R$ 2.500,00',
  },
  {
    nome: 'Elleva - 1 Sessão',
    descricao: 'Bioestimulador de colágeno com resultados duradouros.',
    preco: 'R$ 2.000,00',
  },
  {
    nome: 'Radiesse - 1 Sessão',
    descricao: 'Melhora o contorno facial e a firmeza da pele.',
    preco: 'R$ 1.600,00',
  },
  {
    nome: 'Protocoll',
    descricao: 'Tratamento personalizado para rejuvenescimento.',
    preco: 'R$ 2.600,00',
  },
  { nome: 'Fio Filler (unidade)', descricao: 'Reposição de volume imediato.', preco: 'R$ 350,00' },
  {
    nome: 'Fio de Tração (unidade)',
    descricao: 'Lifting facial sem cirurgia.',
    preco: 'R$ 250,00',
  },
  {
    nome: 'Fio Liso (unidade)',
    descricao: 'Estimula colágeno e melhora textura da pele.',
    preco: 'R$ 150,00',
  },
]

const servicosVisiveis = computed(() => (mostrarTodos.value ? servicos : servicos.slice(0, 6)))
</script>

<style scoped>
a {
  text-decoration: none;
  color: var(--timberwolf);
  font-weight: bold;
  font-size: 0.9rem;
}

.servicos {
  background-color: var(--timberwolf);
  padding: 3rem 1.5rem;
  overflow: hidden;
}

.titulo {
  text-align: center;
  font-size: 2rem;
  color: var(--bronze);
  margin-bottom: 2rem;
  font-weight: 600;
}

.cards-container {
  max-width: 1200px;
  margin: 0 auto;
}

.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

.card {
  background-color: white;
  border-radius: 16px;
  padding: 1.8rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  position: relative;
  overflow: hidden;
}

.card::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(to bottom right, var(--bronze), transparent 70%);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.card:hover::before {
  opacity: 0.1;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
}

.card h3 {
  font-size: 1.2rem;
  color: var(--eerie-black);
  font-weight: 600;
  margin-bottom: 0.5rem;
  position: relative;
  z-index: 1;
}

.card p {
  font-size: 0.95rem;
  color: #444;
  margin-bottom: 1rem;
  line-height: 1.4;
  z-index: 1;
}

.preco {
  font-weight: 600;
  color: var(--bronze);
  font-size: 1.1rem;
  margin-top: auto;
  z-index: 1;
}

.btn {
  background-color: var(--bronze);
  color: white;
  border: none;
  padding: 0.6rem 1.2rem;
  border-radius: 8px;
  cursor: pointer;
  font-weight: 500;
  transition: background 0.3s ease;
  z-index: 1;
}

.btn:hover {
  background-color: var(--eerie-black);
}

.ver-mais-container {
  text-align: center;
  margin-top: 2rem;
}

.btn-toggle {
  background: none;
  border: 2px solid var(--bronze);
  color: var(--eerie-black);
  font-weight: 500;
  padding: 0.6rem 1.4rem;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.btn-toggle:hover {
  background: var(--bronze);
  color: white;
}

/* Animação slide suave */
.slide-enter-active,
.slide-leave-active {
  transition: all 0.5s ease;
}

.slide-enter-from {
  opacity: 0;
  transform: translateY(20px);
}

.slide-leave-to {
  opacity: 0;
  transform: translateY(20px);
}
</style>
