<script setup>
</script>

<template>
  <section id="gallery" class="gallery-section">
    <div class="container section-header">
      <h2 class="section-title">Galeri</h2>
      <p class="section-subtitle">Dari Pohon Aren hingga ke Meja Anda.</p>
    </div>

    <div class="container gallery-grid">
      <!-- Image 1 -->
      <div class="gallery-item large">
        <img src="https://images.unsplash.com/photo-1546255146-2f0855ec6b6f?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Process">
        <div class="overlay">
          <span>Proses Alami</span>
        </div>
      </div>
      <!-- Image 2 -->
      <div class="gallery-item">
        <img src="https://images.unsplash.com/photo-1596707323533-5c7438e8cb22?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Harvest">
        <div class="overlay">
          <span>Panen Tradisional</span>
        </div>
      </div>
      <!-- Image 3 -->
      <div class="gallery-item tall">
        <img src="https://images.unsplash.com/photo-1622483767028-3f66f32aef97?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Texture">
        <div class="overlay">
          <span>Kualitas Premium</span>
        </div>
      </div>
      <!-- Image 4 -->
      <div class="gallery-item">
        <img src="https://images.unsplash.com/photo-1514432324607-a09d9b4aefdd?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Usage">
        <div class="overlay">
          <span>Sajian Nikmat</span>
        </div>
      </div>
      <!-- Image 5 -->
      <div class="gallery-item">
        <img src="https://images.unsplash.com/photo-1497935586351-b67a49e012bf?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Packaging">
        <div class="overlay">
          <span>Kemasan Aman</span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.gallery-section {
  padding: 6rem 0;
  background-color: #FAFAFA; /* Neutral background */
}

.section-header {
  text-align: center;
  margin-bottom: 3rem;
}

.section-title {
  font-size: 2.5rem;
  color: var(--color-brown);
  margin-bottom: 0.5rem;
}

.section-subtitle {
  font-size: 1.1rem;
  color: #777;
  font-style: italic;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 250px;
  gap: 1.5rem;
}

.gallery-item {
  position: relative;
  overflow: hidden;
  border-radius: 12px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.1);
  cursor: pointer;
}

.gallery-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.gallery-item:hover img {
  transform: scale(1.1); /* Hover zoom */
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(62, 44, 35, 0.6);
  opacity: 0;
  transition: opacity 0.3s ease;
  display: flex;
  justify-content: center;
  align-items: center;
}

.gallery-item:hover .overlay {
  opacity: 1;
}

.overlay span {
  color: #fff;
  font-weight: 600;
  font-size: 1.2rem;
  letter-spacing: 1px;
  transform: translateY(20px);
  transition: transform 0.3s ease;
}

.gallery-item:hover .overlay span {
  transform: translateY(0);
}

/* Grid layout variations */
.large {
  grid-column: span 2;
  grid-row: span 2;
}

.tall {
  grid-row: span 2;
}

@media (max-width: 900px) {
  .gallery-grid {
    grid-template-columns: 1fr 1fr;
  }
  .large {
    grid-column: span 2;
  }
}

@media (max-width: 600px) {
  .gallery-grid {
    display: flex;
    flex-direction: column;
  }
  .gallery-item {
    height: 300px;
  }
}
</style>
