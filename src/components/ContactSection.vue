<template>
  <div style="text-align:center">
    <div style="margin-bottom:12px; color:var(--muted)">Hubungi saya melalui:</div>
    <div class="contact-list">
      <a :href="`mailto:${contacts.email}`" class="btn btn-ghost">{{ contacts.email }}</a>
      <a :href="contacts.github" class="btn btn-ghost" target="_blank" rel="noreferrer">GitHub</a>
      <a :href="contacts.linkedin" class="btn btn-ghost" target="_blank" rel="noreferrer">LinkedIn</a>
      <a :href="contacts.instagram" class="btn btn-ghost" target="_blank" rel="noreferrer">Instagram</a>
    </div>
    <div style="margin-top:14px; color:var(--muted)">Atau unduh CV (letakkan file `cv.pdf` di folder `public/`)</div>
    <div style="margin-top:8px">
      <a href="/cv.pdf" class="btn btn-primary" download>Unduh CV</a>
    </div>
  </div>
</template>

<script setup>
import { contacts } from '../data.js'
</script>
