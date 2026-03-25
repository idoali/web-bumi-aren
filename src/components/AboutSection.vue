<script setup>
</script>

<template>
  <section id="about" class="about-section">
    <div class="container about-container">
      <div class="about-image-wrapper">
        <div class="about-image">
          <img src="https://images.unsplash.com/photo-1596707323533-5c7438e8cb22?ixlib=rb-4.0.3&auto=format&fit=crop&w=1080&q=80" alt="Petani menyadap pohon aren">
        </div>
        <div class="image-accent"></div>
      </div>
      <div class="about-content">
        <h2 class="section-title">Tentang Bumi Aren</h2>
        <div class="divider"></div>
        <p class="about-text">
          Bumi Aren lahir dari kekayaan alam Indonesia.
        </p>
        <p class="about-text">
          Kami bekerja langsung dengan petani aren lokal untuk menghasilkan gula aren berkualitas tinggi yang diproses secara alami.
        </p>
        <ul class="about-features">
          <li>
            <span class="icon">🌿</span>
            <span>Tanpa pewarna.</span>
          </li>
          <li>
            <span class="icon">❌</span>
            <span>Tanpa campuran gula lain.</span>
          </li>
          <li>
            <span class="icon">✨</span>
            <span>Tanpa bahan tambahan sintetis.</span>
          </li>
        </ul>
        <p class="about-text highlight">
          Kami percaya bahwa rasa terbaik datang dari proses yang alami dan sederhana.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  background-color: var(--color-cream);
  padding: 6rem 0;
}

.about-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.about-image-wrapper {
  position: relative;
  border-radius: 12px;
}

.about-image {
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 10px 40px rgba(62, 44, 35, 0.15); /* Soft shadow */
  position: relative;
  z-index: 2;
  transition: transform 0.4s ease;
}

.about-image:hover {
  transform: scale(1.02);
}

.about-image img {
  display: block;
  width: 100%;
  height: auto;
  object-fit: cover;
}

.image-accent {
  position: absolute;
  top: -15px;
  left: -15px;
  width: 100%;
  height: 100%;
  border: 2px solid var(--color-gold);
  border-radius: 12px;
  z-index: 1;
}

.about-content {
  text-align: left;
}

.section-title {
  font-size: 2.5rem;
  color: var(--color-brown);
  margin-bottom: 0.5rem;
}

.divider {
  width: 60px;
  height: 3px;
  background-color: var(--color-gold);
  margin-bottom: 1.5rem;
}

.about-text {
  font-size: 1.1rem;
  color: #555;
  margin-bottom: 1rem;
  line-height: 1.8;
}

.about-features {
  list-style: none;
  margin: 1.5rem 0;
  padding: 1.5rem 0;
  border-top: 1px solid rgba(62, 44, 35, 0.1);
  border-bottom: 1px solid rgba(62, 44, 35, 0.1);
}

.about-features li {
  display: flex;
  align-items: center;
  margin-bottom: 0.5rem;
  font-weight: 500;
  color: var(--color-brown);
}

.icon {
  margin-right: 10px;
}

.highlight {
  font-weight: 600;
  color: var(--color-brown);
  font-style: italic;
}

@media (max-width: 900px) {
  .about-container {
    grid-template-columns: 1fr;
  }
}
</style>
