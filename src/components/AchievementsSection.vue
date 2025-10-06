<template>
  <section class="py-12 px-6">
    <h2 class="text-center text-2xl font-bold text-blue-400 mb-6">Pencapaian</h2>
    <ul class="max-w-2xl mx-auto list-disc list-inside text-gray-200 space-y-2">
      <li v-for="(ach, i) in achievements" :key="i">{{ ach }}</li>
    </ul>
  </section>
</template>

<script setup>
import { achievements } from "@/data.js";
</script>
