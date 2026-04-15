<script setup>
</script>

<template>
  <section id="products" class="products-section">
    <div class="container section-header">
      <h2 class="section-title">Produk Unggulan</h2>
      <div class="divider"></div>
      <p class="section-desc">Kualitas terbaik dari alam untuk dapur Anda.</p>
    </div>
    
    <div class="container products-grid">
      <!-- Product 1: Gula Aren Semut -->
      <div class="product-card">
        <div class="product-image">
          <img src="/sample-9.jpeg" alt="Gula Aren Batok">
          <div class="overlay"></div>
        </div>
        <div class="product-info">
          <h3>Gula Aren Batok</h3>
          <p class="product-tag">Traditional Molded</p>
          <p class="product-desc">
            Gula aren batok adalah olahan dari air nira dengan cara tradisional kemudian di cetak dengan cetakan khusus seperti tempurung kelapa atau potongan bambu.  Gula aren batok  memberikan cita rasa yang khas dan aroma yang harum khas nira. Gula aren batok ini sangat cocok digunakan sebagai  pemanis pada minuman dan makanan.
          </p>
          <ul class="product-features">
            <li>Mudah larut</li>
            <li>Warna alami</li>
            <li>Cocok untuk kopi, bakery, dan minuman</li>
          </ul>
        </div>
      </div>

      <!-- Product 2: Sirup Aren -->
      <div class="product-card">
        <div class="product-image">
          <img src="/sample-1.jpeg" alt="Sirup Aren">
          <div class="overlay"></div>
        </div>
        <div class="product-info">
          <h3>Sirup Aren</h3>
          <p class="product-tag">Liquid Nectar</p>
          <p class="product-desc">
            Sirup aren adalah sari manis yang diolah dari nira pohon aren.<br><br>Dibuat melalui proses perebusan perlahan hingga mengental, sirup aren menghadirkan warna cokelat keemasan dengan aroma karamel yang khas dan menggoda.<br><br>Berbeda dengan pemanis buatan, sirup aren memiliki cita rasa yang lebih dalam : manisnya lembut, tidak menusuk, dengan sentuhan smoky dan karamel alami. Inilah yang membuatnya cocok digunakan dalam berbagai sajian, mulai dari minuman tradisional seperti es campur, cendol, dan kopi susu aren, hingga dessert modern seperti pancake, waffle, dan puding.<br><br>Sirup aren kami memiliki warna amber yang cantik, aroma karamel alami, serta rasa manis yang lembut dan tidak meninggalkan aftertaste tajam.<br><br>Profil rasanya yang rich dan complex menjadikannya pilihan ideal sebagai natural sweetener untuk industri beverage, coffee chain, bakery, pastry, dessert, hingga healthy food product.
          </p>
          <ul class="product-features">
            <li>100% natural, tanpa pemanis buatan</li>
            <li>Non-GMO & plant-based</li>
            <li>Diproses secara higienis dan konsisten</li>
            <li>Stabil untuk distribusi jarak jauh</li>
          </ul>
        </div>
      </div>

      <!-- Product 3: Gula Aren Semut -->
      <div class="product-card">
        <div class="product-image">
          <img src="/sample-7.jpeg" alt="Gula Aren Semut">
          <div class="overlay"></div>
        </div>
        <div class="product-info">
          <h3>Gula Aren Semut</h3>
          <p class="product-tag">Granulated Crystal</p>
          <p class="product-desc">
            Gula aren semut adalah produk alami bernilai tinggi yang berasal dari nira pohon aren.
          </p>
          <ul class="product-features">
            <li>Butiran halus &amp; mudah larut</li>
            <li>100% alami tanpa bahan tambahan</li>
            <li>Cocok untuk minuman, kue, dan masakan</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.products-section {
  background-color: #fff;
  padding: 6rem 0;
}

.section-header {
  text-align: center;
  margin-bottom: 4rem;
}

.section-title {
  font-size: 2.5rem;
  color: var(--color-brown);
  margin-bottom: 1rem;
}

.divider {
  width: 80px;
  height: 4px;
  background-color: var(--color-gold);
  margin: 0 auto 1.5rem auto;
}

.section-desc {
  color: #666;
  max-width: 600px;
  margin: 0 auto;
}

.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 3rem;
}

.product-card {
  background: #fff;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0,0,0,0.08); /* Soft shadow */
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  display: flex;
  flex-direction: column;
}

.product-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.12);
}

.product-image {
  height: 300px;
  overflow: hidden;
  position: relative;
}

.product-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.product-card:hover .product-image img {
  transform: scale(1.1); /* Slight zoom */
}

.product-info {
  padding: 2rem;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}

.product-info h3 {
  font-size: 1.8rem;
  color: var(--color-brown);
  margin-bottom: 0.5rem;
}

.product-tag {
  color: var(--color-gold);
  font-weight: 600;
  text-transform: uppercase;
  font-size: 0.8rem;
  letter-spacing: 1px;
  margin-bottom: 1.5rem;
}

.product-desc {
  color: #555;
  margin-bottom: 1.5rem;
  line-height: 1.6;
}

.product-features {
  margin-top: auto;
  list-style: none;
  border-top: 1px solid #eee;
  padding-top: 1rem;
}

.product-features li {
  position: relative;
  padding-left: 1.5rem;
  margin-bottom: 0.5rem;
  color: #444;
  font-size: 0.95rem;
}

.product-features li::before {
  content: '✔';
  position: absolute;
  left: 0;
  color: var(--color-palm);
  font-weight: bold;
}
</style>
