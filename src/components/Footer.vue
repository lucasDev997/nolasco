<script setup>
import { ref } from 'vue'
const year = ref(new Date().getFullYear())
</script>

<template>
  <footer class="footer">
    <p>&copy; {{ year }} Nolasco Vue. All rights reserved.</p>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #42b983;
  padding: 1rem;
  text-align: center;
  color: blue;
  position: fixed;
  width: 100%;
  bottom: 0;
}
</style>
