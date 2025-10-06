<template>
  <section class="hero">
    <div class="container">
      <div class="hero-card">
        <div class="avatar">
          <template v-if="hasPhoto">
            <img :src="profile.photo" alt="foto" style="width:100%; height:100%; object-fit:cover;">
          </template>
          <template v-else>
            {{ initials }}
          </template>
        </div>

        <div class="hero-info">
          <h1>{{ profile.name }}</h1>
          <p class="muted">{{ profile.program }} · {{ profile.university }}</p>
          <p style="margin-top:8px; color:var(--muted)">{{ profile.tagline }}</p>

          <div class="cta-row">
            <a class="btn btn-primary" href="#projects" @click.prevent="$scrollTo('#gallery', 400)">Lihat Karya</a>
            <a class="btn btn-ghost" href="#contact">Kontak</a>
          </div>
        </div>
      </div>

      <div style="margin-top:18px; color:var(--muted)">Tip: ganti data di <code>src/data.js</code> untuk kustomisasi cepat</div>
    </div>
  </section>
</template>

<script setup>
import { profile } from '../data.js'
import { computed } from 'vue'

const hasPhoto = computed(()=> {
  try {
    return !!profile.photo
  } catch { return false }
})

const initials = profile.name.split(' ').map(n => n[0]).slice(0,2).join('').toUpperCase()
</script>
