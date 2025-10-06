<template>
  <section class="hero">
    <div class="container">
      <div class="hero-card">
        <div class="avatar">
          <template v-if="hasPhoto">
            <img
              :src="profile.photo"
              alt="foto"
              class="avatar-img"
            />
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
            <a class="btn btn-primary" href="#gallery" @click.prevent="$scrollTo('#gallery', 400)">Lihat Karya</a>
            <a class="btn btn-ghost" href="#contact">Kontak</a>
            <a class="btn btn-outline" href="/cv.pdf" download>📄 Unduh CV</a>
          </div>
        </div>
      </div>

      <div style="margin-top:18px; color:var(--muted)">
        Tip: ganti data di <code>src/data.js</code> untuk kustomisasi cepat
      </div>
    </div>
  </section>
</template>

<script setup>
import { profile } from '../data.js'
import { computed } from 'vue'

const hasPhoto = computed(() => {
  try {
    return !!profile.photo
  } catch {
    return false
  }
})

const initials = profile.name
  .split(' ')
  .map(n => n[0])
  .slice(0, 2)
  .join('')
  .toUpperCase()
</script>

<style scoped>
.hero {
  padding: 60px 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

.hero-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: rgba(25, 25, 35, 0.8);
  backdrop-filter: blur(12px);
  border-radius: 18px;
  padding: 40px;
  max-width: 420px;
  box-shadow: 0 0 18px rgba(0, 255, 255, 0.1);
  transition: transform 0.3s ease;
}

.hero-card:hover {
  transform: translateY(-5px);
}

.avatar {
  width: 160px;
  height: 160px;
  border-radius: 50%;
  overflow: hidden;
  border: 3px solid cyan;
  margin-bottom: 20px;
}

.avatar-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.hero-info {
  text-align: center;
}

.cta-row {
  display: flex;
  gap: 10px;
  margin-top: 15px;
  flex-wrap: wrap;
  justify-content: center;
}

.btn {
  border: none;
  padding: 10px 16px;
  border-radius: 8px;
  cursor: pointer;
  text-decoration: none;
  font-weight: 600;
}

.btn-primary {
  background: cyan;
  color: #000;
}

.btn-ghost {
  background: transparent;
  border: 1px solid cyan;
  color: cyan;
}

.btn-outline {
  background: transparent;
  border: 1px solid #888;
  color: #bbb;
}

.btn:hover {
  opacity: 0.85;
}
</style>
