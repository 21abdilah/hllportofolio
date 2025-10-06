<template>
  <section class="hero bg-gradient-to-b from-[#050a1f] to-[#0a163a] text-white py-16">
    <div class="container mx-auto px-6 flex flex-col items-center text-center">
      <!-- Foto Profil -->
      <div class="avatar w-40 h-40 mb-6 rounded-full overflow-hidden border-4 border-cyan-400 shadow-[0_0_30px_rgba(0,255,255,0.4)] animate-fade-in">
        <img src="/IMG_20250507_153537.jpg" alt="Foto Profil" class="w-full h-full object-cover" />
      </div>

      <!-- Informasi -->
      <div class="hero-info max-w-xl animate-fade-in-delayed">
        <h1 class="text-3xl font-bold mb-2 tracking-wide text-cyan-300">{{ profile.name }}</h1>
        <p class="text-gray-400">{{ profile.program }} · {{ profile.university }}</p>
        <p class="text-gray-400 mt-3 italic">{{ profile.tagline }}</p>

        <div class="flex justify-center gap-4 mt-6">
          <a class="btn-primary" href="#gallery">Lihat Karya</a>
          <a class="btn-outline" href="#contact">Kontak</a>
        </div>
      </div>

      <p class="mt-10 text-xs text-gray-500">
        Tip: ganti data di <code>src/data.js</code> untuk kustomisasi cepat
      </p>
    </div>
  </section>
</template>

<script setup>
import { profile } from '../data.js'
</script>

<style scoped>
.btn-primary {
  @apply px-5 py-2 bg-cyan-500 hover:bg-cyan-400 text-black font-semibold rounded-lg shadow-lg transition;
}
.btn-outline {
  @apply px-5 py-2 border border-cyan-400 text-cyan-400 hover:bg-cyan-400 hover:text-black font-semibold rounded-lg transition;
}
@keyframes fade-in {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}
.animate-fade-in {
  animation: fade-in 1s ease-out forwards;
}
.animate-fade-in-delayed {
  animation: fade-in 1.5s ease-out 0.2s forwards;
}
</style>
