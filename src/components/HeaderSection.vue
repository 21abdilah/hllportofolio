<template>
  <header class="header-section">
    <div class="profile-card">
      <img
        src="/IMG_20250507_153537.jpg"
        alt="Foto Profil"
        class="profile-img"
      />
      <h1>{{ profile.name }}</h1>
      <p>{{ profile.program }}</p>
      <p class="quote">"{{ profile.interest }}"</p>

      <a href="/cv.pdf" target="_blank" class="cv-button">Unduh CV</a>
    </div>
  </header>
</template>

<script setup>
const profile = {
  name: "Hilal Abdilah",
  program: "Mahasiswa Informatika STIMIK DCI Tasikmalaya",
  interest: "Menjadi insan informatika yang cerdas, kreatif, dan berdaya saing",
};
</script>

<style scoped>
.header-section {
  background: radial-gradient(circle at top, #0a0f1f, #020617);
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 100px 20px;
  min-height: 100vh;
}

.profile-card {
  background: rgba(15, 23, 42, 0.8);
  border: 1px solid #3b82f6;
  border-radius: 20px;
  box-shadow: 0 0 25px rgba(59, 130, 246, 0.3);
  text-align: center;
  padding: 40px 30px;
  max-width: 400px;
  transition: 0.3s;
}

.profile-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 0 40px rgba(59, 130, 246, 0.5);
}

.profile-img {
  width: 180px;
  height: 180px;
  object-fit: cover;
  border-radius: 20px;
  border: 3px solid #3b82f6;
  box-shadow: 0 0 15px rgba(14, 165, 233, 0.5);
  margin-bottom: 20px;
}

.cv-button {
  display: inline-block;
  margin-top: 20px;
  padding: 10px 18px;
  color: #fff;
  background: linear-gradient(135deg, #2563eb, #0ea5e9);
  text-decoration: none;
  border-radius: 12px;
  transition: 0.3s;
}

.cv-button:hover {
  background: linear-gradient(135deg, #0ea5e9, #38bdf8);
  box-shadow: 0 0 15px rgba(59, 130, 246, 0.6);
}
</style>
