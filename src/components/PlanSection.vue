<template>
  <section class="max-w-3xl mx-auto py-12 px-6 text-center">
    <h2 class="text-2xl font-bold text-blue-400 mb-4">Tentang Saya</h2>
    <p class="text-gray-300 leading-relaxed">{{ profile.about }}</p>
  </section>
</template>

<script setup>
import { profile } from "@/data.js";
</script>
