<script setup>
</script>

<template>
  <section id="contact" class="contact-section">
    <div class="container contact-container">
      <h2 class="section-title">Hubungi Kami</h2>
      <p class="contact-subtitle">
        Tertarik untuk bekerja sama atau ingin mencoba sampel produk kami?
        <br>Tim Bumi Aren siap membantu Anda.
      </p>

      <form class="contact-form" @submit.prevent>
        <div class="form-group">
          <input type="text" placeholder="Nama" required>
        </div>
        <div class="form-group">
          <input type="email" placeholder="Email" required>
        </div>
        <div class="form-group">
          <input type="text" placeholder="Perusahaan" required>
        </div>
        <div class="form-group">
          <textarea placeholder="Pesan" rows="5" required></textarea>
        </div>
        <button type="submit" class="btn btn-primary submit-btn">Kirim Pesan</button>
      </form>

      <div class="social-links">
        <a href="#" class="social-icon">WhatsApp</a>
        <a href="#" class="social-icon">Email</a>
        <a href="#" class="social-icon">Instagram</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact-section {
  background-color: var(--color-brown); /* Dark Brown */
  color: #fff;
  padding: 6rem 0;
  text-align: center;
}

.contact-container {
  max-width: 800px;
}

.section-title {
  color: var(--color-gold);
  font-size: 2.5rem;
  margin-bottom: 1.5rem;
}

.contact-subtitle {
  margin-bottom: 3rem;
  font-size: 1.1rem;
  color: #ddd;
  line-height: 1.6;
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  margin-bottom: 3rem;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 1rem 1.5rem;
  border-radius: 8px;
  border: 1px solid rgba(255, 255, 255, 0.2);
  background: rgba(255, 255, 255, 0.05); /* slightly transparent */
  color: #fff;
  font-family: var(--font-body);
  font-size: 1rem;
  transition: all 0.3s ease;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  background: rgba(255, 255, 255, 0.1);
  border-color: var(--color-gold);
}

.form-group input::placeholder,
.form-group textarea::placeholder {
  color: rgba(255, 255, 255, 0.6);
}

.submit-btn {
  width: 100%;
  max-width: 250px;
  align-self: center;
  font-size: 1rem;
  padding: 1rem 2rem;
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 2rem;
  margin-top: 2rem;
  padding-top: 2rem;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
}

.social-icon {
  color: #bbb;
  font-size: 0.9rem;
  text-transform: uppercase;
  letter-spacing: 1px;
  transition: color 0.3s ease;
}

.social-icon:hover {
  color: var(--color-gold);
}

@media (max-width: 600px) {
  .section-title {
    font-size: 2rem;
  }
}
</style>
