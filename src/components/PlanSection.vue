<template>
  <section class="py-12 px-6 text-center">
    <h2 class="text-2xl font-bold text-blue-400 mb-6">Rencana Pemanfaatan Teknologi</h2>
    <div class="grid md:grid-cols-3 gap-6 max-w-5xl mx-auto">
      <div v-for="(desc, key) in plans" :key="key"
           class="bg-blue-800/40 border border-blue-600/30 rounded-lg p-6">
        <h3 class="font-semibold text-lg text-blue-300 capitalize mb-2">{{ key }}</h3>
        <p class="text-gray-300">{{ desc }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import { plans } from "@/data.js";
</script>
