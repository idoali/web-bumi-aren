<script setup>
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import ProductsSection from './components/ProductsSection.vue'
import GallerySection from './components/GallerySection.vue'
import ContactSection from './components/ContactSection.vue'
import ProcessSection from './components/ProcessSection.vue'
import FeaturesSection from './components/FeaturesSection.vue'
</script>

<template>
  <NavBar />
  <main>
    <HeroSection />
    <AboutSection />
    <ProductsSection />
    <ProcessSection />
    <FeaturesSection />
    <GallerySection />
    <ContactSection />
  </main>
  <footer class="main-footer">
    <div class="container">
      <p>&copy; 2026 Bumi Aren. All rights reserved.</p>
    </div>
  </footer>
</template>

<style>
/* Global styles could go here if not in style.css */
.main-footer {
  background-color: #2c1e18; /* Darker than brown */
  color: #888;
  text-align: center;
  padding: 1.5rem 0;
  font-size: 0.9rem;
}
</style>
