<template>
    <!-- Navigation -->
    <nav class="fixed top-4 left-1/2 -translate-x-1/2 w-[95%] md:max-w-6xl bg-white/80 backdrop-blur-lg shadow-lg rounded-lg md:rounded-full z-50 transition-all duration-300">
      <div class="px-6 py-3">
        <div class="flex items-center justify-between">
          <!-- Logo -->
          <div class="flex items-center space-x-3">
            <svg class="w-8 h-8 text-amber-800" viewBox="0 0 24 24" fill="currentColor">
              <path d="M12 2L2 7v10c0 5.55 3.84 10.74 9 12 5.16-1.26 9-6.45 9-12V7l-10-5zm0 2.18l8 4V17c0 4.52-3.1 8.75-7 9.77V4.18H12z"/>
              <circle cx="12" cy="12" r="3"/>
            </svg>
            <span class="text-xl font-bold text-amber-900">Islam Kaukasus</span>
          </div>
          
          <!-- Desktop Menu -->
          <div class="hidden md:flex space-x-6">
            <a href="#hero" class="text-gray-700 hover:text-amber-800 transition font-medium">Beranda</a>
            <a href="#timeline" class="text-gray-700 hover:text-amber-800 transition font-medium">Timeline</a>
            <a href="#tokoh" class="text-gray-700 hover:text-amber-800 transition font-medium">Tokoh</a>
            <a href="#peninggalan" class="text-gray-700 hover:text-amber-800 transition font-medium">Peninggalan</a>
            <a href="#faq" class="text-gray-700 hover:text-amber-800 transition font-medium">FAQ</a>
          </div>

          <!-- Hamburger Button -->
          <button 
            @click="toggleMenu" 
            class="md:hidden p-2 rounded-full hover:bg-amber-100 transition"
            aria-label="Toggle menu"
          >
            <svg 
              class="w-6 h-6 text-amber-900 transition-transform duration-300" 
              :class="{ 'rotate-90': isMenuOpen }"
              fill="none" 
              stroke="currentColor" 
              viewBox="0 0 24 24"
            >
              <path 
                v-if="!isMenuOpen"
                stroke-linecap="round" 
                stroke-linejoin="round" 
                stroke-width="2" 
                d="M4 6h16M4 12h16M4 18h16"
              />
              <path 
                v-else
                stroke-linecap="round" 
                stroke-linejoin="round" 
                stroke-width="2" 
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Menu -->
      <transition
        enter-active-class="transition duration-300 ease-out"
        enter-from-class="opacity-0 -translate-y-4"
        enter-to-class="opacity-100 translate-y-0"
        leave-active-class="transition duration-200 ease-in"
        leave-from-class="opacity-100 translate-y-0"
        leave-to-class="opacity-0 -translate-y-4"
      >
        <div 
          v-if="isMenuOpen" 
          class="md:hidden border-t border-amber-200 px-6 py-4 space-y-3"
        >
          <a 
            href="#hero" 
            @click="closeMenu"
            class="block text-gray-700 hover:text-amber-800 hover:bg-amber-50 transition font-medium py-2 px-4 rounded-lg"
          >
            Beranda
          </a>
          <a 
            href="#timeline" 
            @click="closeMenu"
            class="block text-gray-700 hover:text-amber-800 hover:bg-amber-50 transition font-medium py-2 px-4 rounded-lg"
          >
            Timeline
          </a>
          <a 
            href="#tokoh" 
            @click="closeMenu"
            class="block text-gray-700 hover:text-amber-800 hover:bg-amber-50 transition font-medium py-2 px-4 rounded-lg"
          >
            Tokoh
          </a>
          <a 
            href="#peninggalan" 
            @click="closeMenu"
            class="block text-gray-700 hover:text-amber-800 hover:bg-amber-50 transition font-medium py-2 px-4 rounded-lg"
          >
            Peninggalan
          </a>
          <a 
            href="#faq" 
            @click="closeMenu"
            class="block text-gray-700 hover:text-amber-800 hover:bg-amber-50 transition font-medium py-2 px-4 rounded-lg"
          >
            FAQ
          </a>
        </div>
      </transition>
    </nav>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const closeMenu = () => {
  isMenuOpen.value = false;
};

// Smooth scroll dengan easing yang lebih halus
const smoothScrollTo = (target) => {
  const targetPosition = target.getBoundingClientRect().top + window.pageYOffset;
  const startPosition = window.pageYOffset;
  const distance = targetPosition - startPosition - 100; // offset untuk navbar
  const duration = 800; // durasi dalam ms
  let start = null;

  const easeInOutCubic = (t) => {
    return t < 0.5 
      ? 4 * t * t * t 
      : (t - 1) * (2 * t - 2) * (2 * t - 2) + 1;
  };

  const animation = (currentTime) => {
    if (start === null) start = currentTime;
    const timeElapsed = currentTime - start;
    const progress = Math.min(timeElapsed / duration, 1);
    const ease = easeInOutCubic(progress);
    
    window.scrollTo(0, startPosition + distance * ease);
    
    if (timeElapsed < duration) {
      requestAnimationFrame(animation);
    }
  };

  requestAnimationFrame(animation);
};

onMounted(() => {
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
      e.preventDefault();
      const target = document.querySelector(this.getAttribute('href'));
      if (target) {
        smoothScrollTo(target);
      }
    });
  });
});
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}
</style>