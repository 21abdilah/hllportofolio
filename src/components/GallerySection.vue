<template>
  <section class="gallery-section">
    <div class="gallery">
      <div v-for="(img, i) in gallery" :key="i" class="gallery-item">
        <img :src="img.src" :alt="img.title" />
        <p>{{ img.title }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
const gallery = [
  { src: "/karya1.jpg", title: "Karya Desain 1" },
  { src: "/karya2.jpg", title: "Karya Desain 2" },
];
</script>

<style scoped>
.gallery-section {
  text-align: center;
  padding: 80px 20px;
  background: linear-gradient(to bottom, #0f172a, #020617);
  color: white;
}

.gallery {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 25px;
  margin-top: 40px;
}

.gallery-item {
  background: rgba(15, 23, 42, 0.9);
  border: 1px solid #1e40af;
  border-radius: 12px;
  overflow: hidden;
  width: 280px;
  box-shadow: 0 0 15px rgba(59, 130, 246, 0.2);
  transition: 0.3s;
}

.gallery-item:hover {
  transform: scale(1.05);
  box-shadow: 0 0 25px rgba(59, 130, 246, 0.5);
}

.gallery-item img {
  width: 100%;
  height: 180px;
  object-fit: cover;
}

.gallery-item p {
  padding: 10px;
  background: #1e293b;
  color: #93c5fd;
  font-size: 0.9rem;
}
</style>
