<template>
  <nav class="navbar">
    <div class="container inner">
      <div class="brand">{{ shortBrand }}</div>
      <div class="nav-links">
        <a href="#about">Tentang</a>
        <a href="#skills">Keahlian</a>
        <a href="#achievements">Pencapaian</a>
        <a href="#gallery">Galeri</a>
        <a href="#plans">Rencana</a>
        <a href="#contact">Kontak</a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { profile } from '../data.js'
const shortBrand = profile.name.split(' ')[0] + " • INFORMATIKA"
</script>
