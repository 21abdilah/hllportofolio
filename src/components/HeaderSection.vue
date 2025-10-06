<!-- HeaderSection.vue -->
<template>
  <section class="hero">
    <div class="hero-card">
      <div class="avatar-wrap">
        <template v-if="hasPhoto">
          <img :src="profile.photo" alt="foto" class="avatar-img" />
        </template>
        <template v-else>
          <div class="avatar-placeholder">{{ initials }}</div>
        </template>
      </div>

      <div class="hero-info">
        <h1>{{ profile.name }}</h1>
        <p>{{ profile.title }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import { profile } from '../data.js'

const hasPhoto = !!profile.photo
const initials = profile.name
  .split(' ')
  .map(n => n[0])
  .join('')
  .toUpperCase()
</script>

<style scoped>
.hero {
  padding: 120px 0 60px;
  text-align: center;
}

/* Card */
.hero-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 18px;
  background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
  border: 1px solid var(--glass-border);
  padding: 24px;
  border-radius: 14px;
  box-shadow: 0 8px 40px rgba(2,6,23,0.6);
  backdrop-filter: blur(8px);
  max-width: 320px;
  margin: 0 auto; /* center card */
}

/* Foto profil */
.avatar-wrap {
  width: 140px;
  height: 140px;
  border-radius: 50%;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(180deg, rgba(59,130,246,0.12), rgba(14,165,233,0.08));
  border: 1px solid rgba(255,255,255,0.04);
}

.avatar-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Placeholder huruf inisial */
.avatar-placeholder {
  font-size: 36px;
  font-weight: 700;
  color: var(--accent);
}
</style>
