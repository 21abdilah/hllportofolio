<template>
  <div>
    <div v-for="(a, i) in achievements" :key="i" style="margin-bottom:12px" class="ach">
      <div style="width:8px; height:8px; background:var(--accent); border-radius:2px; margin-top:6px"></div>
      <div>
        <div style="font-weight:600">{{ a }}</div>
        <div style="font-size:12px; color:var(--muted)"</div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { achievements } from '../data.js'
</script>
