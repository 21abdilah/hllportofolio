<template>
  <nav class="navbar fixed top-0 left-0 w-full z-50 bg-gray-900/70 backdrop-blur-md border-b border-cyan-500/20">
    <div class="container mx-auto flex justify-between items-center px-6 py-3">
      <!-- Brand -->
      <div class="text-cyan-400 font-bold text-2xl tracking-widest">{{ shortBrand }}</div>

      <!-- Toggle Button (Mobile) -->
      <button
        @click="toggleMenu"
        class="md:hidden text-cyan-400 hover:text-cyan-300 focus:outline-none transition-colors"
      >
        <svg
          v-if="!menuOpen"
          xmlns="http://www.w3.org/2000/svg"
          class="h-7 w-7"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg
          v-else
          xmlns="http://www.w3.org/2000/svg"
          class="h-7 w-7"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>

      <!-- Links -->
      <div
        :class="[
          'nav-links md:flex md:items-center md:space-x-8 text-gray-300 font-medium text-lg',
          menuOpen ? 'block absolute top-16 left-0 w-full bg-gray-900/95 md:static md:w-auto md:bg-transparent' : 'hidden md:block'
        ]"
      >
        <a
          v-for="link in links"
          :key="link.href"
          :href="link.href"
          class="block md:inline-block px-6 py-3 hover:text-cyan-400 transition-colors"
          @click="closeMenu"
        >
          {{ link.label }}
        </a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
import { profile } from '../data.js'

const shortBrand = profile.name.split(' ')[0]
const menuOpen = ref(false)

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}

const closeMenu = () => {
  menuOpen.value = false
}

const links = [
  { href: '#about', label: 'Tentang' },
  { href: '#skills', label: 'Keahlian' },
  { href: '#achievements', label: 'Pencapaian' },
  { href: '#gallery', label: 'Galeri' },
  { href: '#plans', label: 'Rencana' },
  { href: '#contact', label: 'Kontak' }
]
</script>

<style scoped>
.navbar {
  font-family: 'Orbitron', sans-serif;
  letter-spacing: 0.05em;
}
</style>
