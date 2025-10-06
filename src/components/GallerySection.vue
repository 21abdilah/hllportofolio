<template>
  <div>
    <div v-for="(g, idx) in gallery" :key="idx" class="gallery-card" style="margin-bottom:12px">
      <div style="text-align:center">
        <div style="font-weight:700; color:var(--primary)">{{ g.title }}</div>
        <div style="font-size:13px; color:var(--muted)">{{ g.desc }}</div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { gallery } from '../data.js'
</script>
