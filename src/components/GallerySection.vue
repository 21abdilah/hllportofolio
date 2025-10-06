<template>
  <section class="bg-gradient-to-b from-gray-900 to-blue-950 py-12 px-6">
    <h2 class="text-center text-2xl font-bold text-blue-400 mb-6">Galeri Karya</h2>
    <div class="max-w-5xl mx-auto grid sm:grid-cols-2 md:grid-cols-3 gap-6">
      <div v-for="item in gallery" :key="item.title"
        class="bg-blue-800/40 rounded-lg border border-blue-600/30 overflow-hidden hover:scale-105 transform transition">
        <div class="h-40 flex items-center justify-center bg-blue-950 text-blue-300 italic">
          {{ item.title }}
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { gallery } from "@/data.js";
</script>
