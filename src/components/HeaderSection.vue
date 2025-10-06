<template>
  <header class="text-center py-16 bg-gradient-to-b from-blue-900/70 to-transparent">
    <h1 class="text-4xl font-extrabold text-blue-300 tracking-wide">{{ profile.name }}</h1>
    <p class="text-lg mt-2">{{ profile.program }} · {{ profile.university }}</p>
    <p class="mt-4 italic text-blue-400">“{{ profile.interest }}”</p>
  </header>
</template>

<script setup>
import { profile } from "@/data.js";
</script>
