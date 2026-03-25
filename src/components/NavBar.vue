<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const isMenuOpen = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})

const links = [
  { name: 'Home', href: '#home' },
  { name: 'About', href: '#about' },
  { name: 'Products', href: '#products' },
  { name: 'Gallery', href: '#gallery' },
  { name: 'Contact', href: '#contact' }
]
</script>

<template>
  <nav :class="['navbar', { 'scrolled': isScrolled }]">
    <div class="container nav-container">
      <a href="#" class="branding-group">
        <div class="logo-wrapper">
          <img src="/bumi-aren-logo-crop.svg" alt="Bumi Aren Logo" class="logo-img" />
        </div>
        <div class="motto-container">
          <span class="motto-sub">Natural Energy</span>
          <span class="motto-sub">From the Land of Nusantara</span>
        </div>
      </a>
      
      <div class="hamburger" @click="toggleMenu">
        <span></span>
        <span></span>
        <span></span>
      </div>

      <ul :class="['nav-links', { 'active': isMenuOpen }]">
        <li v-for="link in links" :key="link.name">
          <a :href="link.href" @click="isMenuOpen = false">{{ link.name }}</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 1.5rem 0;
  z-index: 1000;
  transition: all 0.3s ease;
  background: transparent;
}

.navbar.scrolled {
  padding: 1rem 0;
  background: rgba(62, 44, 35, 0.95); /* Dark brown with opacity */
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.branding-group {
  display: flex;
  align-items: center;
  gap: 1.2rem;
  transition: all 0.3s ease;
}

.logo-wrapper {
  height: 55px;
  width: 55px;
  background-color: #fff; /* White background for the logo */
  border-radius: 50%;
  padding: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 15px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.logo-img {
  max-height: 100%;
  max-width: 100%;
}

.logo-wrapper:hover {
  transform: scale(1.05);
}

.motto-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  border-left: 1px solid rgba(255, 255, 255, 0.3);
  padding-left: 1.2rem;
  color: #fff;
  transition: all 0.3s ease;
}

.navbar.scrolled .motto-container {
  border-left-color: rgba(255, 255, 255, 0.1);
}

.motto-sub {
  font-family: var(--font-body);
  font-size: 0.75rem;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 1px;
  opacity: 0.9;
  white-space: nowrap;
  line-height: 1.4;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 2rem;
}

.nav-links li a {
  color: #fff;
  text-transform: uppercase;
  font-size: 0.8rem;
  letter-spacing: 2px;
  font-weight: 500;
  position: relative;
}

.nav-links li a::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background: var(--color-gold);
  transition: width 0.3s ease;
}

.nav-links li a:hover::after {
  width: 100%;
}

.hamburger {
  display: none;
  cursor: pointer;
  flex-direction: column;
  gap: 5px;
}

.hamburger span {
  width: 25px;
  height: 3px;
  background-color: #fff;
  transition: all 0.3s ease;
}

@media (max-width: 768px) {
  .hamburger {
    display: flex;
  }

  .nav-links {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background: var(--color-brown);
    flex-direction: column;
    align-items: center;
    padding: 2rem 0;
    gap: 1.5rem;
    clip-path: circle(0% at 100% 0);
    transition: clip-path 0.5s ease-in-out;
  }

  .nav-links.active {
    clip-path: circle(150% at 100% 0);
  }
}
</style>
