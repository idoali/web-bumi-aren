<script setup>
</script>

<template>
  <section id="home" class="hero-section">
    <div class="hero-bg">
      <div class="hero-overlay"></div>
      <div class="hero-content container">
        <h1 class="hero-title">Manis Alami dari Pohon Aren Indonesia.</h1>
        <p class="hero-subtitle">Gula aren premium tanpa pewarna, tanpa campuran, tanpa bahan kimia.</p>
        <div class="hero-buttons">
          <a href="#products" class="btn btn-primary">Lihat Produk</a>
          <a href="#contact" class="btn btn-outline">Hubungi Kami</a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  position: relative;
  height: 100vh;
  width: 100%;
  padding: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.hero-bg {
  background-image: url('/gula-aren-bg.jpg'); /* Coffee/Sugar aesthetic as placeholder */
  background-size: cover;
  background-position: center;
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to bottom, rgba(0,0,0,0.3) 0%, rgba(0,0,0,0.3) 10%,  rgba(0,0,0,0.3) 20%, rgba(0,0,0,0.8) 100%);
  z-index: 1;
}

.hero-content {
  position: relative;
  z-index: 2;
  text-align: center;
  color: #fff;
  max-width: 800px;
  animation: fadeInUp 1s ease-out;
}

.hero-title {
  font-size: 3.5rem; /* Large bold typography */
  line-height: 1.2;
  margin-bottom: 1.5rem;
  font-weight: 700;
  text-shadow: 0 2px 10px rgba(0,0,0,0.5);
}

.hero-subtitle {
  font-size: 1.2rem;
  font-weight: 300; /* Light weight body */
  margin-bottom: 2.5rem;
  opacity: 0.9;
  letter-spacing: 0.5px;
}

.hero-buttons {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 2.5rem;
  }
}
</style>
