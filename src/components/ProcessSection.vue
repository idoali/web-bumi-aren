<script setup>
import { ref } from 'vue'

const activeTab = ref('batok')
</script>

<template>
  <section id="process" class="process-section">
    <div class="container section-header process-header">
      <h2 class="section-title text-cream">Proses Pembuatan</h2>
      <div class="divider"></div>
      <p class="section-desc text-cream-light">
        Dedikasi di setiap tetes nira, menghadirkan kemurnian ke meja Anda.
      </p>
    </div>

    <div class="container process-container">
      <div class="process-tabs">
        <button 
          @click="activeTab = 'batok'" 
          :class="['tab-button', activeTab === 'batok' ? 'active' : '']"
        >
          Gula Aren Batok
        </button>
        <button
          @click="activeTab = 'sirup'"
          :class="['tab-button', activeTab === 'sirup' ? 'active' : '']"
        >
          Sirup Aren
        </button>
        <button
          @click="activeTab = 'semut'"
          :class="['tab-button', activeTab === 'semut' ? 'active' : '']"
        >
          Gula Aren Semut
        </button>
      </div>

      <div class="process-content" v-if="activeTab === 'batok'">
        <div class="stepper-container">
          <!-- Step 1 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">1</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Pemilihan dan Penyadapan Nira Aren</h3>
              <ul>
                <li>Proses dimulai dari pohon aren (Arenga pinnata) yang sudah cukup umur, biasanya 5-10 tahun.</li>
                <li>Tandan bunga jantan dipukul-pukul selama beberapa hari untuk merangsang keluarnya nira.</li>
                <li>Ujung tandan kemudian diiris tipis.</li>
                <li>Nira ditampung menggunakan bambu atau jerigen bersih.</li>
                <li>Penyadapan dilakukan 2 kali sehari (pagi dan sore).</li>
                <li class="important"><strong>Penting:</strong> Wadah harus bersih agar nira tidak cepat asam.</li>
              </ul>
            </div>
          </div>
          
          <!-- Step 2 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">2</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Penyaringan Nira</h3>
              <ul>
                <li>Nira segar disaring menggunakan kain halus untuk memisahkan kotoran seperti serangga atau serpihan bunga.</li>
              </ul>
            </div>
          </div>

          <!-- Step 3 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">3</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Perebusan</h3>
              <ul>
                <li>Nira dimasukkan ke dalam wajan besar (biasanya dari besi atau baja).</li>
                <li>Dimasak dengan api sedang sambil terus diaduk.</li>
                <li>Proses perebusan berlangsung 2-4 jam tergantung jumlah nira.</li>
                <li class="nested-list">
                  <strong>Selama proses ini:</strong>
                  <ul>
                    <li>Buih akan muncul dan harus dibuang.</li>
                    <li>Warna berubah dari putih keruh menjadi cokelat keemasan.</li>
                    <li>Aroma karamel alami mulai tercium.</li>
                  </ul>
                </li>
              </ul>
            </div>
          </div>

          <!-- Step 4 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">4</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Pengentalan</h3>
              <ul>
                <li>Saat volume menyusut dan tekstur mengental seperti karamel, api dikecilkan.</li>
                <li>Pengadukan harus konstan agar tidak gosong.</li>
                <li class="nested-list">
                  <strong>Tanda sudah siap cetak:</strong>
                  <ul>
                    <li>Cairan lebih kental dan berat saat diaduk.</li>
                    <li>Jika diteteskan ke air, langsung mengeras.</li>
                  </ul>
                </li>
              </ul>
            </div>
          </div>

          <!-- Step 5 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">5</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Pencetakan</h3>
              <ul>
                <li>Cairan gula dituangkan ke dalam cetakan batok kelapa.</li>
                <li>Dibiarkan dingin dan mengeras secara alami (±30-60 menit).</li>
                <li>Setelah keras, gula dilepaskan dari cetakan dan siap dikemas.</li>
              </ul>
            </div>
          </div>
          
          <div class="stepper-conclusion glass-morphism-card shadow-premium">
            <p><strong>Hasilnya:</strong> Gula aren batok padat, beraroma khas, tahan lama, dan siap digunakan untuk minuman atau masakan tradisional.</p>
          </div>
        </div>
      </div>

      <div class="process-content" v-else-if="activeTab === 'sirup'">
        <div class="stepper-container">
          <!-- Step 1 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">1</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Penyadapan dan Penyaringan</h3>
              <ul>
                <li>Proses awal sama seperti gula batok: penyadapan dan penyaringan nira segar.</li>
              </ul>
            </div>
          </div>
          
          <!-- Step 2 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">2</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Perebusan dengan Kontrol Suhu</h3>
              <ul>
                <li>Nira direbus dengan api sedang.</li>
                <li>Diaduk perlahan agar tidak meluap.</li>
                <li>Buih dibuang secara berkala.</li>
                <li class="important"><strong>Perbedaannya:</strong> Proses dihentikan sebelum terlalu kental.</li>
              </ul>
            </div>
          </div>

          <!-- Step 3 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">3</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Pengentalan Ringan</h3>
              <ul>
                <li class="nested-list">
                  <strong>Tekstur yang diinginkan adalah:</strong>
                  <ul>
                    <li>Lebih kental dari air.</li>
                    <li>Namun tetap cair dan mudah dituang.</li>
                    <li>Biasanya membutuhkan waktu 1,5-3 jam tergantung volume.</li>
                  </ul>
                </li>
              </ul>
            </div>
          </div>

          <!-- Step 4 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">4</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Penyaringan Ulang</h3>
              <ul>
                <li>Setelah mencapai kekentalan yang pas, sirup disaring kembali agar hasilnya halus dan bersih.</li>
              </ul>
            </div>
          </div>

          <!-- Step 5 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">5</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Pendinginan dan Pengemasan</h3>
              <ul>
                <li>Sirup didinginkan hingga suhu ruang.</li>
                <li>Dimasukkan ke botol steril.</li>
                <li>Ditutup rapat untuk menjaga kualitas dan daya tahan.</li>
              </ul>
            </div>
          </div>
          
          <div class="stepper-conclusion glass-morphism-card shadow-premium">
            <p><strong>Hasilnya:</strong> Sirup aren berwarna cokelat pekat, rasa manis legit alami, cocok untuk kopi, es campur, kolak, atau dessert modern.</p>
          </div>
        </div>
      </div>

      <div class="process-content" v-else-if="activeTab === 'semut'">
        <div class="stepper-container">
          <!-- Step 1 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">1</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Penyadapan Nira</h3>
              <ul>
                <li>Nira diambil dari tandan bunga Arenga pinnata pagi atau sore hari.</li>
                <li>Penyadap memanjat pohon untuk mengambil nira segar yang ditampung dalam wadah bersih.</li>
                <li class="important"><strong>Penting:</strong> Kebersihan alat sangat penting agar nira tidak cepat asam dan kualitas gula tetap terjaga.</li>
              </ul>
            </div>
          </div>

          <!-- Step 2 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">2</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Penyaringan Nira</h3>
              <ul>
                <li>Nira yang terkumpul disaring untuk memisahkan kotoran seperti serat, debu, atau serpihan alami.</li>
                <li>Proses ini penting agar hasil akhir lebih bersih dan higienis.</li>
              </ul>
            </div>
          </div>

          <!-- Step 3 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">3</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Pemasakan Nira</h3>
              <ul>
                <li>Nira yang sudah disaring dimasak di atas tungku dengan api sedang sambil terus diaduk perlahan.</li>
                <li>Tujuan pemasakan adalah mengurangi kadar air hingga cairan berubah menjadi kental dan berwarna cokelat keemasan.</li>
                <li class="important"><strong>Penting:</strong> Pembuat gula harus teliti menjaga suhu agar nira tidak gosong dan rasa manis alaminya tetap terjaga.</li>
              </ul>
            </div>
          </div>

          <!-- Step 4 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">4</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Pengkristalan (Pembentukan Butiran)</h3>
              <ul>
                <li>Ketika cairan mulai mengental dan mencapai tekstur tertentu, proses pengadukan diperkuat agar adonan berubah menjadi butiran halus.</li>
                <li>Dari tahap ini muncul bentuk khas "gula semut", yaitu butiran kecil yang menyerupai sarang semut.</li>
              </ul>
            </div>
          </div>

          <!-- Step 5 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">5</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Pengayakan dan Pendinginan</h3>
              <ul>
                <li>Gula diayak untuk menghasilkan ukuran yang seragam.</li>
                <li>Kemudian didinginkan agar kadar air stabil dan produk tidak menggumpal saat disimpan.</li>
                <li class="important"><strong>Penting:</strong> Tahap ini sangat penting supaya produk tidak menggumpal saat disimpan.</li>
              </ul>
            </div>
          </div>

          <!-- Step 6 -->
          <div class="stepper-item interaction-lift">
            <div class="stepper-number">6</div>
            <div class="stepper-card shadow-premium glass-morphism-card">
              <h3>Pengemasan dan Pengecekan Kualitas</h3>
              <ul>
                <li>Gula aren semut masuk ke tahap pengemasan dalam plastik food grade, standing pouch, atau botol.</li>
                <li class="nested-list">
                  <strong>Pada kemasan perlu dicantumkan:</strong>
                  <ul>
                    <li>Nama produk</li>
                    <li>Berat bersih</li>
                    <li>Tanggal produksi</li>
                    <li>Masa simpan</li>
                    <li>Komposisi</li>
                    <li>Izin usaha (jika ada)</li>
                  </ul>
                </li>
                <li>Kemasan yang rapi akan meningkatkan kepercayaan pembeli.</li>
                <li>Pengecekan kualitas dilakukan melalui inspeksi rasa, aroma, warna, dan kebersihan.</li>
              </ul>
            </div>
          </div>

          <div class="stepper-conclusion glass-morphism-card shadow-premium">
            <p><strong>Hasilnya:</strong> Gula aren semut siap dipasarkan dengan kualitas rasa yang khas, kemasan menarik, serta peluang distribusi ke pasar tradisional, toko oleh-oleh, maupun marketplace online.</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.process-section {
  background-color: var(--color-charcoal);
  padding: 6rem 0;
  color: var(--color-cream);
  position: relative;
  overflow: hidden;
}

.process-header {
  text-align: center;
  margin-bottom: 3rem;
  position: relative;
  z-index: 2;
}

.text-cream {
  color: var(--color-cream);
}

.text-cream-light {
  color: #ccc;
  max-width: 600px;
  margin: 0 auto;
}

.divider {
  width: 80px;
  height: 4px;
  background-color: var(--color-gold);
  margin: 0 auto 1.5rem auto;
}

.process-container {
  position: relative;
  z-index: 2;
}

.process-tabs {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-bottom: 4rem;
}

.tab-button {
  background: transparent;
  border: 2px solid var(--color-gold);
  color: var(--color-gold);
  padding: 0.8rem 2.5rem;
  border-radius: 50px;
  font-size: 1rem;
  font-weight: 600;
  letter-spacing: 1px;
}

.tab-button:hover,
.tab-button.active {
  background: var(--color-gold);
  color: #fff;
  box-shadow: 0 4px 15px rgba(201, 162, 39, 0.4);
}

.stepper-container {
  display: flex;
  flex-direction: column;
  gap: 2.5rem;
  position: relative;
  max-width: 800px;
  margin: 0 auto;
}

.stepper-container::before {
  content: '';
  position: absolute;
  top: 0;
  bottom: 0;
  left: 30px;
  width: 2px;
  background: rgba(201, 162, 39, 0.3); /* gold line */
  z-index: 0;
}

.stepper-item {
  display: flex;
  align-items: flex-start;
  position: relative;
  z-index: 1;
}

.stepper-number {
  width: 60px;
  height: 60px;
  min-width: 60px;
  background: var(--color-charcoal);
  border: 2px solid var(--color-gold);
  color: var(--color-gold);
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.8rem;
  font-weight: 700;
  font-family: var(--font-heading);
  margin-right: 2rem;
  box-shadow: 0 4px 10px rgba(0,0,0,0.5);
  transition: all 0.3s ease;
}

.stepper-item:hover .stepper-number {
  background: var(--color-gold);
  color: #fff;
}

.stepper-card {
  flex-grow: 1;
  padding: 2rem;
  border-radius: 15px;
  background: #1e1e1e;
  border: 1px solid rgba(255,255,255,0.05);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.glass-morphism-card {
  background: rgba(255, 255, 255, 0.03);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.08);
}

.stepper-card h3 {
  color: var(--color-gold);
  font-size: 1.4rem;
  margin-bottom: 1rem;
  font-family: var(--font-heading);
}

.stepper-card ul {
  list-style: none;
  padding: 0;
}

.stepper-card ul li {
  position: relative;
  padding-left: 1.5rem;
  margin-bottom: 0.6rem;
  color: #ddd;
  font-size: 1rem;
}

.stepper-card ul li::before {
  content: '•';
  position: absolute;
  left: 0;
  color: var(--color-gold);
  font-size: 1.2rem;
  line-height: 1;
}

.important strong {
  color: var(--color-gold-premium);
}

.nested-list {
  margin-top: 1rem;
}

.nested-list ul {
  margin-top: 0.5rem;
  margin-bottom: 0.5rem;
}

.nested-list ul li::before {
  content: '◦';
  color: #aaa;
}

.stepper-conclusion {
  margin-top: 2rem;
  padding: 1.5rem 2rem;
  border-radius: 12px;
  border-left: 4px solid var(--color-gold);
  color: var(--color-cream);
  font-size: 1.1rem;
  line-height: 1.6;
}

.stepper-conclusion strong {
  color: var(--color-gold);
}

@media (max-width: 768px) {
  .stepper-container::before {
    left: 20px;
  }
  .stepper-number {
    width: 40px;
    height: 40px;
    min-width: 40px;
    font-size: 1.2rem;
    margin-right: 1rem;
  }
  .stepper-card {
    padding: 1.5rem;
  }
}
</style>
