<script setup>
import { ref } from 'vue'
const year = ref(new Date().getFullYear())
</script>

<template>
  <footer class="footer">
    <div class="footer-container">
      <div class="footer-info">
        <h3 class="footer-title">Nolasco Body Face</h3>
        <p>Localizada na Av. Brigadeiro Lima e Silva, 1642 — Loja B, Duque de Caxias (RJ)</p>
        <p>Agendamentos podem ser feitos pelo telefone <strong>(21) 96673-4959</strong>.</p>
      </div>

      <div class="footer-contact">
        <h3>Entre em contato</h3>
        <p>Telefone: (21) 96673-4959</p>
        <div class="footer-social">
          <a
            href="https://wa.me/5521966734959?text=Ol%C3%A1%2C%20tenho%20interesse%20no%20procedimento%20e%20gostaria%20de%20mais%20informa%C3%A7%C3%B5es%20para%20agendar.%20Pode%20me%20ajudar%3F"
            target="_blank"
            rel="noopener noreferrer"
            class="social-link whatsapp"
            title="WhatsApp"
          >
            <img src="../assets/icons/whatsapp.svg" alt="WhatsApp" />
          </a>

          <a
            href="https://www.instagram.com/"
            target="_blank"
            rel="noopener noreferrer"
            class="social-link instagram"
            title="Instagram"
          >
            <img src="../assets/icons/instagram.svg" alt="Instagram" />
          </a>
        </div>
      </div>
    </div>

    <div class="footer-bottom">
      <p>&copy; {{ year }} Nolasco Body Face — Todos os direitos reservados.</p>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background: linear-gradient(135deg, var(--bronze), var(--timberwolf));
  color: var(--eerie-black);
  padding: 40px 20px 20px;
  font-family: 'Poppins', sans-serif;
}

.footer-container {
  display: flex;
  justify-content: space-evenly;
  align-items: top;
  flex-direction: column;
  gap: 30px;
  max-width: 1100px;
  margin: 0 auto;
}

.footer-info,
.footer-contact {
  flex: 1;
}

.footer-title {
  color: var(--timberwolf);
  font-size: 1.5rem;
  margin-bottom: 10px;
}
.footer-contact h3 {
  margin-bottom: 10px;
  font-size: 1.5rem;
  color: var(--timberwolf);
}
.footer-social {
  display: flex;
  gap: 15px;
  margin-top: 10px;
}

.social-link img {
  width: 30px;
  height: 30px;
  transition: transform 0.2s ease;
}

.social-link:hover img {
  transform: scale(1.1);
}

.footer-bottom {
  text-align: center;
  font-size: 0.9rem;
  margin-top: 30px;
  border-top: 1px solid rgba(0, 0, 0, 0.1);
  padding-top: 10px;
}

@media (min-width: 768px) {
  .footer-container {
    flex-direction: row;
    justify-content: space-between;
  }
}
</style>
