<template>
  <section id="gallery" class="bg-[#060d28] text-white py-16">
    <div class="container mx-auto px-6 text-center">
      <h2 class="text-2xl font-bold mb-8 text-cyan-300 tracking-wide">Pencapaian & Dokumentasi Visual</h2>

      <div class="grid md:grid-cols-2 gap-8">
        <img src="/karya1.jpg" alt="Karya 1" class="rounded-2xl shadow-[0_0_25px_rgba(0,255,255,0.3)] hover:scale-105 transition-transform duration-300">
        <img src="/karya2.jpg" alt="Karya 2" class="rounded-2xl shadow-[0_0_25px_rgba(0,255,255,0.3)] hover:scale-105 transition-transform duration-300">
      </div>

      <div class="mt-10 text-left max-w-xl mx-auto space-y-4">
        <div v-for="(a, i) in achievements" :key="i" class="flex items-start gap-3 bg-[#0b1a3f] p-4 rounded-lg shadow-md hover:shadow-[0_0_15px_rgba(0,255,255,0.2)] transition">
          <div class="w-2 h-2 bg-cyan-400 rounded-sm mt-2"></div>
          <div>
            <div class="font-semibold">{{ a }}</div>
            <div class="text-xs text-gray-400">— dokumentasi & catatan</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { achievements } from '../data.js'
</script>
