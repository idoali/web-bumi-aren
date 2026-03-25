<script setup>
</script>

<template>
  <section id="features" class="features-section">
    <div class="container">
      <div class="features-grid-wrapper">
        <!-- Tips Menjaga Kualitas -->
        <div class="feature-block tips-block">
          <div class="block-header">
            <h3>Tips Menjaga Kualitas</h3>
            <div class="mini-divider"></div>
          </div>
          <div class="tips-grid">
            <div class="tip-card interaction-lift shadow-premium">
              <div class="tip-icon">⏱️</div>
              <p>Gunakan nira segar maksimal <strong>3-4 jam</strong> setelah penyadapan.</p>
            </div>
            <div class="tip-card interaction-lift shadow-premium">
              <div class="tip-icon">🔥</div>
              <p>Gunakan <strong>api stabil</strong> agar tidak gosong selama perebusan.</p>
            </div>
            <div class="tip-card interaction-lift shadow-premium">
              <div class="tip-icon">💧</div>
              <p>Hindari <strong>kontaminasi air</strong> saat proses pencetakan.</p>
            </div>
            <div class="tip-card interaction-lift shadow-premium">
              <div class="tip-icon">📦</div>
              <p>Simpan produk di tempat <strong>kering dan sejuk</strong>.</p>
            </div>
          </div>
        </div>

        <!-- Keunggulan Gula Aren -->
        <div class="feature-block usp-block">
          <div class="block-header text-right">
            <h3>Keunggulan Gula Aren</h3>
            <div class="mini-divider right"></div>
          </div>
          <div class="usp-list">
            <div class="usp-item interaction-lift">
              <div class="usp-icon">✔</div>
              <div class="usp-content">
                <h4>Tanpa Pemutih</h4>
                <p>Proses alami menghasilkan warna cokelat khas tanpa zat kimia berbahaya.</p>
              </div>
            </div>
            <div class="usp-item interaction-lift">
              <div class="usp-icon">✔</div>
              <div class="usp-content">
                <h4>Tanpa Pengawet</h4>
                <p>Ketahanan alami didapat dari proses kristalisasi yang tepat.</p>
              </div>
            </div>
            <div class="usp-item interaction-lift">
              <div class="usp-icon">✔</div>
              <div class="usp-content">
                <h4>Mineral Alami</h4>
                <p>Kaya nutrisi penting dan mineral yang sangat bermanfaat bagi tubuh.</p>
              </div>
            </div>
            <div class="usp-item interaction-lift">
              <div class="usp-icon">✔</div>
              <div class="usp-content">
                <h4>Indeks Glikemik Rendah</h4>
                <p>Lebih sehat dan relatif aman dikonsumsi dibanding gula pasir biasa.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.features-section {
  background-color: var(--color-cream-light);
  padding: 6rem 0;
}

.features-grid-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
}

.block-header h3 {
  font-size: 2rem;
  color: var(--color-brown);
  margin-bottom: 0.5rem;
  font-family: var(--font-heading);
}

.mini-divider {
  width: 50px;
  height: 3px;
  background-color: var(--color-gold);
  margin-bottom: 2rem;
}

.mini-divider.right {
  margin-left: auto;
}

.text-right {
  text-align: right;
}

/* Tips Block */
.tips-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
}

.tip-card {
  background: #fff;
  padding: 1.5rem;
  border-radius: 12px;
  text-align: center;
  border: 1px solid rgba(0,0,0,0.05);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.tip-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.tip-card p {
  color: #555;
  font-size: 0.95rem;
  line-height: 1.5;
}

.tip-card strong {
  color: var(--color-brown);
}

/* USP Block */
.usp-list {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.usp-item {
  display: flex;
  align-items: flex-start;
  background: #fff;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.03);
}

.usp-icon {
  background: var(--color-gold);
  color: #fff;
  width: 35px;
  height: 35px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1rem;
  font-weight: bold;
  margin-right: 1.5rem;
  flex-shrink: 0;
  margin-top: 0.2rem;
}

.usp-content h4 {
  color: var(--color-brown);
  font-size: 1.2rem;
  margin-bottom: 0.3rem;
  font-family: var(--font-heading);
}

.usp-content p {
  color: #666;
  font-size: 0.95rem;
  line-height: 1.5;
}

@media (max-width: 992px) {
  .features-grid-wrapper {
    grid-template-columns: 1fr;
    gap: 5rem;
  }
  
  .block-header.text-right {
    text-align: left;
  }
  
  .mini-divider.right {
    margin-left: 0;
  }
}

@media (max-width: 576px) {
  .tips-grid {
    grid-template-columns: 1fr;
  }
}
</style>
