<template>
  <nav class="navbar">
    <div class="container inner">
      <div class="brand">{{ shortBrand }}</div>

      <!-- Toggle Button -->
      <button class="nav-toggle" @click="toggleMenu">
        <svg v-if="!menuOpen" xmlns="http://www.w3.org/2000/svg" width="26" height="26" fill="none" stroke="var(--accent)" stroke-width="2">
          <path stroke-linecap="round" d="M4 6h18M4 12h18M4 18h18" />
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" width="26" height="26" fill="none" stroke="var(--accent)" stroke-width="2">
          <path stroke-linecap="round" d="M6 6l12 12M6 18L18 6" />
        </svg>
      </button>

      <!-- Links -->
      <div :class="['nav-links', { open: menuOpen }]">
        <a href="#about" @click="closeMenu">Tentang</a>
        <a href="#skills" @click="closeMenu">Keahlian</a>
        <a href="#achievements" @click="closeMenu">Pencapaian</a>
        <a href="#gallery" @click="closeMenu">Galeri</a>
        <a href="#plans" @click="closeMenu">Rencana</a>
        <a href="#contact" @click="closeMenu">Kontak</a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
import { profile } from '../data.js'

const shortBrand = profile.name.split(' ')[0]
const menuOpen = ref(false)
const toggleMenu = () => (menuOpen.value = !menuOpen.value)
const closeMenu = () => (menuOpen.value = false)
</script>

<style scoped>
.nav-toggle {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
}

@media (max-width: 768px) {
  .nav-links {
    display: none;
    flex-direction: column;
    gap: 10px;
    position: absolute;
    top: 60px;
    left: 0;
    right: 0;
    padding: 18px 0;
    background: rgba(2, 6, 23, 0.95);
    border-top: 1px solid rgba(255, 255, 255, 0.03);
    animation: fadeSlide 0.3s ease;
  }

  .nav-links.open {
    display: flex;
  }

  .nav-toggle {
    display: block;
  }

  @keyframes fadeSlide {
    from {
      opacity: 0;
      transform: translateY(-10px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
}
</style>
