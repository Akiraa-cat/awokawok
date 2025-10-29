<template>
    <!-- Navigation -->
    <nav class="fixed top-0 w-full bg-white/90 backdrop-blur-md shadow-md z-50">
      <div class="container mx-auto px-6 py-4">
        <div class="flex items-center justify-between">
          <div class="flex items-center space-x-3">
            <svg class="w-8 h-8 text-amber-800" viewBox="0 0 24 24" fill="currentColor">
              <path d="M12 2L2 7v10c0 5.55 3.84 10.74 9 12 5.16-1.26 9-6.45 9-12V7l-10-5zm0 2.18l8 4V17c0 4.52-3.1 8.75-7 9.77V4.18H12z"/>
              <circle cx="12" cy="12" r="3"/>
            </svg>
            <span class="text-xl font-bold text-amber-900">Islam Kaukasus</span>
          </div>
          <div class="hidden md:flex space-x-6">
            <a href="#hero" class="text-gray-700 hover:text-amber-800 transition font-medium">Beranda</a>
            <a href="#timeline" class="text-gray-700 hover:text-amber-800 transition font-medium">Timeline</a>
            <a href="#tokoh" class="text-gray-700 hover:text-amber-800 transition font-medium">Tokoh</a>
            <a href="#peninggalan" class="text-gray-700 hover:text-amber-800 transition font-medium">Peninggalan</a>
            <a href="#faq" class="text-gray-700 hover:text-amber-800 transition font-medium">FAQ</a>
          </div>
        </div>
      </div>
    </nav>
</template>

<script setup>
onMounted(() => {
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
      e.preventDefault();
      const target = document.querySelector(this.getAttribute('href'));
      if (target) {
        target.scrollIntoView({
          behavior: 'smooth',
          block: 'start'
        });
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