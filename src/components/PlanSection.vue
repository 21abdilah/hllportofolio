<template>
  <div>
    <div class="plan-card" v-for="(val,key) in plans" :key="key" style="margin-bottom:12px; padding:12px; border-radius:10px; border:1px solid rgba(255,255,255,0.02);">
      <div style="font-weight:700; color:var(--primary); text-transform:capitalize">{{ key }}</div>
      <div style="color:var(--muted); margin-top:6px">{{ val }}</div>
    </div>
  </div>
</template>

<script setup>
import { plans } from '../data.js'
</script>
