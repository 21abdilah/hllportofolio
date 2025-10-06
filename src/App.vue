<template>
  <main class="min-h-screen text-gray-100">
    <HeaderSection />
    <AboutSection />
    <SkillsSection />
    <AchievementsSection />
    <GallerySection />
    <PlanSection />
    <footer class="text-center py-6 text-sm text-gray-400 border-t border-gray-700 mt-8">
      © 2025 Hilal Abdilah · Portofolio
    </footer>
  </main>
</template>

<script setup>
import HeaderSection from "@/components/HeaderSection.vue";
import AboutSection from "@/components/AboutSection.vue";
import SkillsSection from "@/components/SkillsSection.vue";
import AchievementsSection from "@/components/AchievementsSection.vue";
import GallerySection from "@/components/GallerySection.vue";
import PlanSection from "@/components/PlanSection.vue";
</script>
