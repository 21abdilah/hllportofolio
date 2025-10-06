<template>
  <div>
    <div v-for="(s, i) in skills" :key="i" class="skill" style="margin-bottom:12px">
      <div style="display:flex; justify-content:space-between; align-items:center">
        <div style="font-weight:600">{{ s }}</div>
        <div style="font-size:12px; color:var(--muted)">Level: Dasar</div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { skills } from '../data.js'
</script>
