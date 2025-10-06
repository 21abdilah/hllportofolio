<template>
  <div class="panel">
    <h3 style="margin-top:0">Tentang Saya</h3>
    <p style="color:var(--muted)">{{ profile.about }}</p>
  </div>
</template>

<script setup>
import { profile } from '../data.js'
</script>
