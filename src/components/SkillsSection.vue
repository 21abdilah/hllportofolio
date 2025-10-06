<template>
  <section class="bg-gradient-to-t from-blue-950/50 to-transparent py-12">
    <h2 class="text-center text-2xl font-bold text-blue-400 mb-6">Keahlian & Minat</h2>
    <ul class="max-w-2xl mx-auto grid md:grid-cols-2 gap-4 px-6">
      <li v-for="(skill, i) in skills" :key="i"
          class="bg-blue-800/40 border border-blue-600/40 rounded-lg p-4 hover:bg-blue-700/50 transition">
        {{ skill }}
      </li>
    </ul>
  </section>
</template>

<script setup>
import { skills } from "@/data.js";
</script>
