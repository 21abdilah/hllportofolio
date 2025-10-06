<template>
  <div>
    <Navbar />
    <main>
      <HeaderSection />
      <section id="about" class="section container">
        <AboutSection />
      </section>

      <section id="skills" class="section container">
        <h2>Keahlian & Minat</h2>
        <div class="panel grid-3">
          <SkillsSection />
        </div>
      </section>

      <section id="achievements" class="section container">
        <h2>Pencapaian</h2>
        <div class="panel">
          <AchievementsSection />
        </div>
      </section>

      <section id="gallery" class="section container">
        <h2>Dokumentasi Visual</h2>
        <div class="panel grid-3">
          <GallerySection />
        </div>
      </section>

      <section id="plans" class="section container">
        <h2>Rencana Pemanfaatan Teknologi</h2>
        <div class="panel grid-3">
          <PlanSection />
        </div>
      </section>

      <section id="contact" class="section container">
        <h2>Kontak & Link</h2>
        <div class="panel">
          <ContactSection />
        </div>
      </section>

      <footer class="footer container">
        © {{ new Date().getFullYear() }} {{ profile.name }}
      </footer>
    </main>
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import HeaderSection from './components/HeaderSection.vue'
import AboutSection from './components/AboutSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import AchievementsSection from './components/AchievementsSection.vue'
import GallerySection from './components/GallerySection.vue'
import PlanSection from './components/PlanSection.vue'
import ContactSection from './components/ContactSection.vue'
import { profile } from './data.js'
</script>
