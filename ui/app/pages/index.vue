<template>
  <div class="min-h-screen bg-gradient-to-b from-amber-50 via-white to-amber-50">
    
    <!-- Islamic Pattern Background -->
    <div class="fixed inset-0 opacity-5 pointer-events-none z-0">
      <div class="absolute inset-0" style="background-image: url('data:image/svg+xml,%3Csvg width=\'60\' height=\'60\' viewBox=\'0 0 60 60\' xmlns=\'http://www.w3.org/2000/svg\'%3E%3Cg fill=\'none\' fill-rule=\'evenodd\'%3E%3Cg fill=\'%23000000\' fill-opacity=\'1\'%3E%3Cpath d=\'M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v6h4v4h2V6h4V4H6z\'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E'); background-size: 60px 60px;"></div>
    </div>

    <!-- Hero Section with Typing Effect -->
    <section id="hero" class="relative min-h-screen flex items-center justify-center px-6 pt-20">
      <div class="absolute inset-0 bg-gradient-to-br from-amber-100 via-orange-50 to-amber-200 opacity-50"></div>
      <div class="container mx-auto max-w-6xl text-center relative z-10">
        <div class="mb-8">
          <svg class="w-24 h-24 mx-auto mb-6 text-amber-800" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 1L3 5v6c0 5.55 3.84 10.74 9 12 5.16-1.26 9-6.45 9-12V5l-9-4z"/>
            <circle cx="12" cy="11" r="3" fill="white"/>
          </svg>
          <h1 class="text-5xl md:text-7xl font-bold text-amber-900 mb-6">
            <span class="typing-text">{{ displayText }}</span>
            <span class="cursor" :class="{ 'cursor-blink': !isTyping }">|</span>
          </h1>
          <div class="w-32 h-1 bg-amber-600 mx-auto mb-8"></div>
        </div>
        
        <p class="text-2xl md:text-3xl text-gray-800 mb-6 font-semibold">
          Menelusuri Jejak Islam di Persimpangan Dua Benua
        </p>
        
        <p class="text-xl text-gray-600 max-w-3xl mx-auto mb-12">
          Dari pegunungan Kaukasus yang megah hingga benteng-benteng kuno, temukan perjalanan luar biasa penyebaran Islam di perbatasan Eropa dan Asia
        </p>

        <!-- CTA Buttons -->
        <div class="flex flex-wrap justify-center gap-4 mt-8 sm:mt-10">
          <!-- Button: Mulai Jelajahi -->
          <a
            href="#timeline"
            class="flex items-center justify-center gap-2 bg-amber-800 hover:bg-amber-900 
                  text-white font-semibold px-6 sm:px-8 py-3 sm:py-4 rounded-full 
                  text-base sm:text-lg transition-all duration-300 transform 
                  hover:scale-105 hover:shadow-[0_0_20px_rgba(251,191,36,0.5)] w-full sm:w-auto"
          >
            <svg class="w-5 h-5 sm:w-6 sm:h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"/>
            </svg>
            Mulai Jelajahi
          </a>

          <!-- Button: Lihat Peninggalan -->
          <a
            href="#peninggalan"
            class="flex items-center justify-center gap-2 bg-white hover:bg-amber-50 
                  text-amber-900 font-semibold px-6 sm:px-8 py-3 sm:py-4 rounded-full 
                  text-base sm:text-lg transition-all duration-300 transform 
                  hover:scale-105 hover:shadow-[0_0_20px_rgba(251,191,36,0.3)] border-2 border-amber-800 w-full sm:w-auto"
          >
            <svg class="w-5 h-5 sm:w-6 sm:h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/>
            </svg>
            Lihat Peninggalan
          </a>
        </div>

        <!-- Stats Cards -->
        <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mt-16 max-w-4xl mx-auto">
          <div class="bg-white/80 backdrop-blur-sm rounded-xl p-6 shadow-lg">
            <svg class="w-8 h-8 text-amber-700 mx-auto mb-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
            </svg>
            <div class="text-3xl font-bold text-amber-900">13</div>
            <div class="text-sm text-gray-600">Abad Sejarah</div>
          </div>
          <div class="bg-white/80 backdrop-blur-sm rounded-xl p-6 shadow-lg">
            <svg class="w-8 h-8 text-amber-700 mx-auto mb-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"/>
            </svg>
            <div class="text-3xl font-bold text-amber-900">50+</div>
            <div class="text-sm text-gray-600">Tokoh Penting</div>
          </div>
          <div class="bg-white/80 backdrop-blur-sm rounded-xl p-6 shadow-lg">
            <svg class="w-8 h-8 text-amber-700 mx-auto mb-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/>
            </svg>
            <div class="text-3xl font-bold text-amber-900">100+</div>
            <div class="text-sm text-gray-600">Peninggalan</div>
          </div>
          <div class="bg-white/80 backdrop-blur-sm rounded-xl p-6 shadow-lg">
            <svg class="w-8 h-8 text-amber-700 mx-auto mb-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"/>
            </svg>
            <div class="text-3xl font-bold text-amber-900">5</div>
            <div class="text-sm text-gray-600">Negara</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Timeline Section -->
    <section id="timeline" class="relative py-20 px-6 bg-white">
      <div class="container mx-auto max-w-6xl">
        <div class="text-center mb-16">
          <svg class="w-16 h-16 text-amber-800 mx-auto mb-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
          </svg>
          <h2 class="text-4xl md:text-5xl font-bold text-amber-900 mb-4">Timeline Sejarah Islam di Kaukasus</h2>
          <p class="text-xl text-gray-600 max-w-3xl mx-auto">Perjalanan panjang Islam dari abad ke-7 hingga masa kini</p>
        </div>

        <!-- Interactive Timeline -->
        <div class="relative">
          <!-- Timeline Line -->
          <div class="absolute left-1/2 transform -translate-x-1/2 w-1 h-full bg-gradient-to-b from-amber-300 via-amber-600 to-amber-900 hidden md:block"></div>

          <!-- Timeline Items -->
          <div v-for="(event, index) in timelineEvents" :key="index" class="relative mb-12">
            <div :class="['flex items-center', index % 2 === 0 ? 'md:flex-row' : 'md:flex-row-reverse']">
              
              <!-- Content Card -->
              <div class="w-full md:w-5/12 bg-white rounded-2xl shadow-xl p-6 border-2 border-amber-200 hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-2">
                <div class="flex items-center gap-3 mb-4">
                  <div class="bg-amber-100 rounded-full p-3">
                    <svg class="w-6 h-6 text-amber-800" fill="currentColor" viewBox="0 0 20 20">
                      <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"/>
                      <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"/>
                    </svg>
                  </div>
                  <h3 class="text-2xl font-bold text-amber-900">{{ event.year }}</h3>
                </div>
                <h4 class="text-xl font-semibold text-gray-800 mb-3">{{ event.title }}</h4>
                <p class="text-gray-600 leading-relaxed">{{ event.description }}</p>
                <div v-if="event.details" class="mt-4 pt-4 border-t border-amber-100">
                  <ul class="space-y-2">
                    <li v-for="(detail, idx) in event.details" :key="idx" class="flex items-start gap-2 text-sm text-gray-600">
                      <svg class="w-4 h-4 text-amber-600 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
                      </svg>
                      <span>{{ detail }}</span>
                    </li>
                  </ul>
                </div>
              </div>

              <!-- Timeline Dot -->
              <div class="hidden md:block absolute left-1/2 transform -translate-x-1/2 w-6 h-6 bg-amber-600 rounded-full border-4 border-white shadow-lg z-10"></div>

              <!-- Spacer -->
              <div class="hidden md:block w-5/12"></div>
            </div>
          </div>
        </div>
      </div>
    </section>

<!-- Character Selection Section - Tokoh -->
<section id="tokoh" class="relative min-h-screen flex items-center justify-center overflow-hidden">
  
  <!-- Full Background Image with Dissolve Transition -->
  <transition name="bg-dissolve" mode="out-in">
    <div :key="currentHero" class="absolute inset-0">
      <img :src="heroes[currentHero].background" :alt="heroes[currentHero].name" class="w-full h-full object-cover">
      <div class="absolute inset-0 bg-gradient-to-b from-black/70 via-black/50 to-black/80"></div>
    </div>
  </transition>

  <!-- Animated Geometric Shapes -->
  <div class="absolute inset-0 overflow-hidden pointer-events-none">
    <!-- Floating Circles - Responsive sizes -->
    <div class="absolute top-10 sm:top-20 left-5 sm:left-10 w-32 h-32 sm:w-48 sm:h-48 md:w-64 md:h-64 border-2 sm:border-4 border-amber-400/20 rounded-full animate-float"></div>
    <div class="absolute top-20 sm:top-40 right-10 sm:right-20 w-48 h-48 sm:w-64 sm:h-64 md:w-96 md:h-96 border-2 sm:border-4 border-orange-400/15 rounded-full animate-float-delayed"></div>
    <div class="absolute bottom-16 sm:bottom-32 left-1/4 w-32 h-32 sm:w-48 sm:h-48 border-2 sm:border-4 border-amber-300/25 rounded-full animate-float-slow"></div>
    
    <!-- Geometric Lines -->
    <svg class="absolute top-0 left-0 w-full h-full opacity-10">
      <line x1="0" y1="0" x2="100%" y2="100%" stroke="url(#gradient1)" stroke-width="2"/>
      <line x1="100%" y1="0" x2="0" y2="100%" stroke="url(#gradient2)" stroke-width="2"/>
      <defs>
        <linearGradient id="gradient1" x1="0%" y1="0%" x2="100%" y2="100%">
          <stop offset="0%" style="stop-color:#f59e0b;stop-opacity:0" />
          <stop offset="50%" style="stop-color:#f59e0b;stop-opacity:1" />
          <stop offset="100%" style="stop-color:#f59e0b;stop-opacity:0" />
        </linearGradient>
        <linearGradient id="gradient2" x1="0%" y1="0%" x2="100%" y2="100%">
          <stop offset="0%" style="stop-color:#fb923c;stop-opacity:0" />
          <stop offset="50%" style="stop-color:#fb923c;stop-opacity:1" />
          <stop offset="100%" style="stop-color:#fb923c;stop-opacity:0" />
        </linearGradient>
      </defs>
    </svg>

    <!-- Hexagons - Responsive sizes -->
    <div class="absolute top-1/4 right-5 sm:right-10 animate-pulse-slow">
      <svg width="60" height="60" viewBox="0 0 100 100" class="sm:w-20 sm:h-20 md:w-[100px] md:h-[100px] text-amber-400/20">
        <path d="M50 0 L93.3 25 L93.3 75 L50 100 L6.7 75 L6.7 25 Z" fill="none" stroke="currentColor" stroke-width="3"/>
      </svg>
    </div>
    <div class="absolute bottom-1/3 left-8 sm:left-16 animate-pulse-slower">
      <svg width="50" height="50" viewBox="0 0 100 100" class="sm:w-16 sm:h-16 md:w-20 md:h-20 text-orange-400/20">
        <path d="M50 0 L93.3 25 L93.3 75 L50 100 L6.7 75 L6.7 25 Z" fill="none" stroke="currentColor" stroke-width="3"/>
      </svg>
    </div>

    <!-- Rotating Star - Responsive size -->
    <svg class="absolute top-1/3 left-1/4 sm:left-1/3 w-20 h-20 sm:w-24 sm:h-24 md:w-32 md:h-32 text-amber-400/10 animate-spin-very-slow" viewBox="0 0 100 100">
      <polygon points="50,5 61,35 92,35 67,55 78,85 50,65 22,85 33,55 8,35 39,35" fill="currentColor"/>
    </svg>
  </div>

  <!-- Content Container -->
  <div class="relative z-10 w-full px-3 sm:px-4 md:px-6 lg:px-4 py-12 sm:py-16 md:py-20">
    
    <!-- Header -->
    <div class="text-center mb-8 sm:mb-10 md:mb-12">
      <div class="inline-flex items-center justify-center w-12 h-12 sm:w-14 sm:h-14 md:w-16 md:h-16 bg-amber-500/20 backdrop-blur-sm rounded-full mb-3 sm:mb-4 border-2 border-amber-400/50">
        <svg class="w-6 h-6 sm:w-7 sm:h-7 md:w-8 md:h-8 text-amber-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"/>
        </svg>
      </div>
      <h2 class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-2 sm:mb-3 drop-shadow-lg px-2" style="font-family: 'Playfair Display', serif;">Tokoh-Tokoh Penting</h2>
      <p class="text-base sm:text-lg md:text-xl text-amber-200 drop-shadow-md px-4" style="font-family: 'Inter', sans-serif;">Para pahlawan yang membentuk sejarah Islam di Kaukasus</p>
    </div>

    <!-- Character Display -->
    <div class="max-w-7xl mx-auto">
      <transition name="slide-up-hero" mode="out-in">
        <div :key="currentHero" class="grid grid-cols-1 lg:grid-cols-12 gap-4 sm:gap-6 md:gap-8 items-start">
          
          <!-- Avatar Navigation - Show on Mobile/Tablet Only -->
          <div class="lg:hidden flex flex-row justify-center items-center gap-3 sm:gap-4 order-1 pb-4">
            <button 
              v-for="(hero, idx) in heroes" 
              :key="idx" 
              @click="selectHero(idx)" 
              :class="['relative group transition-all duration-300', currentHero === idx ? 'scale-110' : 'hover:scale-105']"
              :aria-label="`Pilih ${hero.name}`"
            >
              <!-- Avatar Container -->
              <div :class="['w-14 h-14 sm:w-16 sm:h-16 md:w-20 md:h-20 rounded-full overflow-hidden border-3 sm:border-4 transition-all duration-300 shadow-lg', currentHero === idx ? 'border-amber-400 shadow-amber-500/70 ring-2 sm:ring-4 ring-amber-400/40' : 'border-white/50 hover:border-amber-300']">
                <img :src="hero.avatarImage" :alt="hero.name" class="w-full h-full object-cover">
              </div>
              
              <!-- Hover Tooltip -->
              <div class="absolute left-1/2 -translate-x-1/2 -top-12 sm:-top-14 bg-black/95 text-white px-3 sm:px-4 py-1.5 sm:py-2 rounded-xl text-xs sm:text-sm whitespace-nowrap opacity-0 group-hover:opacity-100 transition-opacity pointer-events-none shadow-2xl border border-amber-400/50 z-20" style="font-family: 'Inter', sans-serif;">
                {{ hero.name.split(' ').slice(0, 2).join(' ') }}
                <div class="absolute left-1/2 -translate-x-1/2 -bottom-1.5 w-3 h-3 bg-black/95 rotate-45 border-r border-b border-amber-400/50"></div>
              </div>
            </button>
          </div>
          
          <!-- Left: Character Info -->
          <div class="lg:col-span-4 text-center lg:text-left space-y-4 sm:space-y-5 md:space-y-6 order-3 lg:order-1">
            <div class="space-y-3 sm:space-y-4">
              <!-- Period Badge -->
              <div class="inline-block">
                <span class="px-4 sm:px-5 py-1.5 sm:py-2 bg-gradient-to-r from-amber-500 via-orange-500 to-amber-500 text-white rounded-full text-xs sm:text-sm font-bold shadow-2xl border-2 border-amber-300 whitespace-nowrap" style="font-family: 'Inter', sans-serif;">
                  {{ heroes[currentHero].period }}
                </span>
              </div>

              <!-- Name -->
              <h3 class="text-2xl sm:text-3xl md:text-4xl lg:text-5xl font-bold text-white leading-tight drop-shadow-lg px-2 lg:px-0" style="font-family: 'Playfair Display', serif;">
                {{ heroes[currentHero].name }}
              </h3>

              <!-- Role -->
              <p class="text-lg sm:text-xl md:text-2xl font-semibold text-amber-300 drop-shadow-md px-2 lg:px-0" style="font-family: 'Playfair Display', serif;">
                {{ heroes[currentHero].role }}
              </p>

              <!-- Divider -->
              <div class="w-20 sm:w-24 h-0.5 sm:h-1 bg-gradient-to-r from-amber-400 via-orange-400 to-transparent mx-auto lg:mx-0"></div>

              <!-- Description -->
              <p class="text-xs sm:text-sm md:text-base text-gray-200 leading-relaxed drop-shadow-md px-4 lg:px-0" style="font-family: 'Inter', sans-serif;">
                {{ heroes[currentHero].description }}
              </p>

              <!-- Contributions -->
              <div class="space-y-2 sm:space-y-3 px-2 lg:px-0">
                <h4 class="text-sm sm:text-base md:text-lg font-semibold text-amber-300 flex items-center gap-2 justify-center lg:justify-start" style="font-family: 'Playfair Display', serif;">
                  <svg class="w-4 h-4 sm:w-5 sm:h-5" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd"/>
                  </svg>
                  Kontribusi & Warisan
                </h4>
                <div class="space-y-1.5 sm:space-y-2">
                  <div v-for="(contribution, idx) in heroes[currentHero].contributions" :key="idx" class="flex items-start gap-2 bg-black/40 backdrop-blur-md border border-amber-400/30 rounded-lg p-2 sm:p-3 hover:bg-black/50 hover:border-amber-400/50 transition-all shadow-lg text-left">
                    <svg class="w-3 h-3 sm:w-4 sm:h-4 text-amber-400 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
                    </svg>
                    <p class="text-xs sm:text-sm text-gray-100 font-medium" style="font-family: 'Inter', sans-serif;">{{ contribution }}</p>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Center: Character Image -->
          <div class="lg:col-span-6 flex justify-center items-end order-2 lg:order-2">
            <div class="relative">
              <!-- Stage Spotlights Shooting Upward -->
              <div class="absolute bottom-0 left-1/2 transform -translate-x-1/2 w-[250%] h-[180%] pointer-events-none overflow-visible">
                <!-- Main spotlight beam -->
                <div class="absolute bottom-0 left-1/2 transform -translate-x-1/2 w-[70%] h-full spotlight-beam-center"></div>
                
                <!-- Left spotlight -->
                <div class="absolute bottom-0 left-[15%] w-[50%] h-full spotlight-beam-left"></div>
                
                <!-- Right spotlight -->
                <div class="absolute bottom-0 right-[15%] w-[50%] h-full spotlight-beam-right"></div>
                
                <!-- Animated pulsing center beam -->
                <div class="absolute bottom-0 left-1/2 transform -translate-x-1/2 w-[60%] h-full spotlight-beam-pulse"></div>
                
                <!-- Additional soft fill lights -->
                <div class="absolute bottom-0 left-[25%] w-[30%] h-full spotlight-beam-fill-left"></div>
                <div class="absolute bottom-0 right-[25%] w-[30%] h-full spotlight-beam-fill-right"></div>
                
                <!-- Ground glow -->
                <div class="absolute bottom-0 left-1/2 transform -translate-x-1/2 w-[120%] h-20 sm:h-24 md:h-32 bg-gradient-radial from-amber-400/40 via-orange-400/20 to-transparent blur-3xl"></div>
                
                <!-- Secondary ground glow -->
                <div class="absolute bottom-0 left-1/2 transform -translate-x-1/2 w-[100%] h-24 sm:h-32 md:h-40 bg-gradient-radial from-yellow-300/30 via-amber-300/15 to-transparent blur-3xl"></div>
              </div>
              
              <!-- Character Image Container with Show Up & Float Animation -->
              <div :key="currentHero" class="relative animate-float-character">
                <div class="relative w-56 h-80 sm:w-64 sm:h-96 md:w-80 md:h-[450px] lg:w-96 lg:h-[550px]">
                  <transition name="character-show-up" mode="out-in">
                    <!-- Character image with shadow -->
                    <img :src="heroes[currentHero].characterImage" :alt="heroes[currentHero].name" class="w-full h-full object-cover object-top">
                  </transition>
                  <!-- Subtle vignette effect -->
                  <div class="absolute inset-0 via-transparent to-transparent rounded-2xl pointer-events-none"></div>
                </div>
              </div>
              
              <!-- Additional Rim Light Effects -->
              <div class="absolute top-0 left-0 w-full h-20 sm:h-24 md:h-32 bg-gradient-to-b from-amber-400/10 to-transparent blur-xl pointer-events-none"></div>
              <div class="absolute bottom-0 left-0 w-full h-32 sm:h-40 md:h-48 bg-gradient-to-t from-orange-500/20 to-transparent blur-2xl pointer-events-none"></div>
            </div>
          </div>

          <!-- Right: Avatar Navigation - Desktop Only -->
          <div class="hidden lg:flex lg:col-span-2 lg:flex-col justify-center lg:justify-start items-center gap-3 sm:gap-4 order-4">
            <button 
              v-for="(hero, idx) in heroes" 
              :key="idx" 
              @click="selectHero(idx)" 
              :class="['relative group transition-all duration-300', currentHero === idx ? 'scale-110' : 'hover:scale-105']"
              :aria-label="`Pilih ${hero.name}`"
            >
              <!-- Avatar Container -->
              <div :class="['w-14 h-14 sm:w-16 sm:h-16 md:w-20 md:h-20 rounded-full overflow-hidden border-3 sm:border-4 transition-all duration-300 shadow-lg', currentHero === idx ? 'border-amber-400 shadow-amber-500/70 ring-2 sm:ring-4 ring-amber-400/40' : 'border-white/50 hover:border-amber-300']">
                <img :src="hero.avatarImage" :alt="hero.name" class="w-full h-full object-cover">
              </div>
              
              <!-- Hover Tooltip -->
              <div class="absolute left-1/2 -translate-x-1/2 -top-12 sm:-top-14 bg-black/95 text-white px-3 sm:px-4 py-1.5 sm:py-2 rounded-xl text-xs sm:text-sm whitespace-nowrap opacity-0 group-hover:opacity-100 transition-opacity pointer-events-none shadow-2xl border border-amber-400/50 z-20" style="font-family: 'Inter', sans-serif;">
                {{ hero.name.split(' ').slice(0, 2).join(' ') }}
                <div class="absolute left-1/2 -translate-x-1/2 -bottom-1.5 w-3 h-3 bg-black/95 rotate-45 border-r border-b border-amber-400/50"></div>
              </div>
            </button>
          </div>
        </div>
      </transition>
    </div>
  </div>
</section>

        <!-- Peninggalan Section -->
    <section id="peninggalan" class="relative py-20 px-6 bg-white">
      <div class="container mx-auto max-w-6xl">
        <div class="text-center mb-16" data-aos="fade-up">
          <svg class="w-16 h-16 text-amber-800 mx-auto mb-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/>
          </svg>
          <h2 class="text-4xl md:text-5xl font-bold text-amber-900 mb-4">Peninggalan Bersejarah</h2>
          <p class="text-xl text-gray-600 max-w-3xl mx-auto">Jejak peradaban Islam yang masih berdiri kokoh hingga kini</p>
        </div>

        <!-- Heritage Grid -->
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div v-for="(heritage, index) in heritages" :key="index" class="group" data-aos="fade-up" :data-aos-delay="index * 100">
            <div class="bg-white rounded-2xl overflow-hidden shadow-lg hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-2 border border-amber-100">
              <div class="relative h-64 overflow-hidden bg-gray-200">
                <img :src="heritage.image" :alt="heritage.name" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
                <div class="absolute bottom-4 left-4 right-4">
                  <div class="flex items-center gap-2 text-white text-sm">
                    <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd"/>
                    </svg>
                    <span>{{ heritage.location }}</span>
                  </div>
                </div>
              </div>
              <div class="p-6">
                <div class="flex items-center gap-2 text-amber-700 text-sm mb-2">
                  <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd"/>
                  </svg>
                  <span>{{ heritage.year }}</span>
                </div>
                <h3 class="text-xl font-bold text-amber-900 mb-3 group-hover:text-amber-700 transition">{{ heritage.name }}</h3>
                <p class="text-gray-600 text-sm leading-relaxed">{{ heritage.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- FAQ Section -->
    <section id="faq" class="relative py-20 px-6 bg-gradient-to-b from-amber-50 to-white">
      <div class="container mx-auto max-w-4xl">
        <div class="text-center mb-16">
          <svg class="w-16 h-16 text-amber-800 mx-auto mb-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"/>
          </svg>
          <h2 class="text-4xl md:text-5xl font-bold text-amber-900 mb-4">Pertanyaan yang Sering Diajukan</h2>
          <p class="text-xl text-gray-600">Temukan jawaban atas pertanyaan umum tentang Islam di Kaukasus</p>
        </div>

        <div class="space-y-4">
          <div v-for="(faq, index) in faqs" :key="index" class="bg-white rounded-xl shadow-md overflow-hidden border border-amber-100">
            <button @click="toggleFAQ(index)" class="w-full px-6 py-5 flex items-center justify-between hover:bg-amber-50 transition">
              <span class="text-left font-semibold text-gray-800">{{ faq.question }}</span>
              <svg :class="['w-6 h-6 text-amber-700 transition-transform', openFAQ === index ? 'transform rotate-180' : '']" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
              </svg>
            </button>
            <transition name="accordion">
              <div v-if="openFAQ === index" class="px-6 pb-5">
                <p class="text-gray-600 leading-relaxed">{{ faq.answer }}</p>
              </div>
            </transition>
          </div>
        </div>
      </div>
    </section>

    <!-- Sources Section -->
    <section id="sumber" class="relative py-20 px-6 bg-white">
      <div class="container mx-auto max-w-4xl">
        <div class="text-center mb-12">
          <svg class="w-16 h-16 text-amber-800 mx-auto mb-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"/>
          </svg>
          <h2 class="text-4xl md:text-5xl font-bold text-amber-900 mb-4">Sumber & Referensi</h2>
          <p class="text-xl text-gray-600">Informasi dikompilasi dari berbagai sumber terpercaya</p>
        </div>

        <div class="bg-gradient-to-br from-amber-50 to-orange-50 rounded-2xl p-8 shadow-lg">
          <div class="space-y-4">
            <div v-for="(source, index) in sources" :key="index" class="flex items-start gap-3 p-4 bg-white rounded-lg hover:shadow-md transition">
              <svg class="w-5 h-5 text-amber-700 mt-1 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
              </svg>
              <div class="flex-1">
                <p class="text-gray-700 text-sm leading-relaxed">{{ source }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

// Typing effect data
const texts = [
  'Sejarah Islam di Kaukasus',
  'Perbatasan Eropa dan Asia',
  'Pegunungan yang Megah',
  'Peradaban Islam',
  'Jejak Sejarah Kaukasus'
];

const displayText = ref('');
const currentIndex = ref(0);
const charIndex = ref(0);
const isTyping = ref(true);
const isDeleting = ref(false);
let typingTimeout;

const typeEffect = () => {
  const currentText = texts[currentIndex.value];
  
  if (!isDeleting.value) {
    if (charIndex.value < currentText.length) {
      displayText.value = currentText.substring(0, charIndex.value + 1);
      charIndex.value++;
      isTyping.value = true;
      typingTimeout = setTimeout(typeEffect, 100);
    } else {
      isTyping.value = false;
      typingTimeout = setTimeout(() => {
        isDeleting.value = true;
        typeEffect();
      }, 2500);
    }
  } else {
    if (charIndex.value > 0) {
      displayText.value = currentText.substring(0, charIndex.value - 1);
      charIndex.value--;
      isTyping.value = true;
      typingTimeout = setTimeout(typeEffect, 60);
    } else {
      isDeleting.value = false;
      currentIndex.value = (currentIndex.value + 1) % texts.length;
      typingTimeout = setTimeout(typeEffect, 500);
    }
  }
};

// Timeline Events Data
const timelineEvents = ref([
  {
    year: '640-660 M',
    title: 'Penaklukan Awal Arab',
    description: 'Pasukan Islam di bawah Khilafah Rasyidun pertama kali memasuki wilayah Kaukasus setelah menaklukkan Persia Sasanid.',
    details: [
      'Khalifah Umar bin Khattab mengirim ekspedisi ke utara',
      'Penaklukan kota Derbent (Bab al-Abwab)',
      'Pembentukan garnisun Arab pertama'
    ]
  },
  {
    year: '700-800 M',
    title: 'Periode Konsolidasi',
    description: 'Islam mulai berakar di wilayah Dagestan dan Azerbaijan utara melalui perdagangan dan diplomasi.',
    details: [
      'Pembangunan Masjid Juma Derbent (salah satu masjid tertua di Rusia)',
      'Suku-suku lokal mulai memeluk Islam',
      'Bahasa Arab menjadi bahasa ilmu pengetahuan'
    ]
  },
  {
    year: '1000-1200 M',
    title: 'Penyebaran ke Pegunungan',
    description: 'Islam menyebar ke wilayah pegunungan Chechnya dan Ingushetia melalui ulama dari Dagestan.',
    details: [
      'Dinasti Shirvanshah mendukung dakwah Islam',
      'Pembangunan madrasah dan pusat pendidikan',
      'Penerjemahan teks-teks Islam ke bahasa lokal'
    ]
  },
  {
    year: '1500-1700 M',
    title: 'Masa Keemasan',
    description: 'Islam menjadi identitas utama masyarakat Kaukasus di tengah persaingan Ottoman dan Safawi.',
    details: [
      'Pembangunan masjid-masjid megah',
      'Berkembangnya tarekat Naqsyabandiyah dan Qadiriyah',
      'Penguatan hukum Syariah dalam masyarakat'
    ]
  },
  {
    year: '1785-1859 M',
    title: 'Perang Kaukasus',
    description: 'Perlawanan heroik Muslim Kaukasus melawan ekspansi Kekaisaran Rusia dipimpin oleh Imam Shamil.',
    details: [
      'Sheikh Mansur memulai perlawanan (1785-1791)',
      'Imam Shamil memimpin Imamat Kaukasus selama 25 tahun',
      'Penerapan sistem pemerintahan Islam yang terorganisir'
    ]
  },
  {
    year: '1920-1991 M',
    title: 'Era Soviet',
    description: 'Islam menghadapi tekanan berat dari rezim komunis Soviet, namun tetap bertahan dalam hati masyarakat.',
    details: [
      'Penutupan masjid dan madrasah',
      'Penindasan terhadap ulama dan praktik keagamaan',
      'Islam bertahan secara underground dan dalam keluarga'
    ]
  },
  {
    year: '1991-Sekarang',
    title: 'Kebangkitan Islam',
    description: 'Pasca runtuhnya Uni Soviet, Islam mengalami kebangkitan dan menjadi kekuatan utama di Kaukasus.',
    details: [
      'Pembangunan kembali masjid dan lembaga pendidikan',
      'Peningkatan kesadaran keislaman di kalangan generasi muda',
      'Islam sebagai identitas budaya dan politik'
    ]
  }
]);

// Heroes/Characters Data
const currentHero = ref(0);

const heroes = ref([
  {
    name: "Sasongko Alfauzan Sudirayuda",
    period: "Abad ke-7 M",
    role: "Panglima Ekspedisi Arab ke Kaukasus",
    description: "Komandan Arab pada periode Rashidun yang memimpin ekspedisi ke kawasan Derbent dan menghadapi Khazar — tokoh penting dalam gelombang awal penyebaran Islam ke wilayah utara Kaukasus.",
    background: "/images/abd-alrahman-bg.jpg",
    characterImage: "/images/abd-alrahman.png",
    avatarImage: "/images/abd-alrahman-avt.jpg",
    contributions: [
      "Memimpin operasi militer ke Derbent dan wilayah utara Kaukasus",
      "Terlibat dalam konflik awal Arab–Khazar yang menentukan pengaruh regional",
      "Sumber penting dalam kronik Tabari dan studi sejarah Arab-Kaukasus"
    ]
  },
  {
    name: "Imam Shamil",
    period: "1797-1871 M",
    role: "Imam & Pemimpin Perlawanan Kaukasus",
    description: "Pemimpin politik, militer, dan spiritual (Naqshbandi) yang memimpin perlawanan Dagestan & Chechnya melawan Rusia selama puluhan tahun — simbol perlawanan Islam di Kaukasus abad ke-19.",
    background: "/images/imam-bg.jpg",
    characterImage: "/images/imam.png",
    avatarImage: "/images/imam-avt.jpeg",
    contributions: [
      "Memimpin Imamat Kaukasus (sebagai pemimpin Murid/Naqshbandi) 1830-an sampai 1859",
      "Menyatukan suku-suku Dagestan & Chechnya dalam perlawanan terorganisir",
      "Meninggalkan warisan hukum & pendidikan agama lokal"
    ]
  },
  {
    name: "Sheikh Mansur (Ushurma)",
    period: "1760-1794 M",
    role: "Ulama-Militer & Pelopor Perlawanan",
    description: "Ulama dari Chechnya yang memimpin gerakan awal melawan penetrasi Rusia — menggabungkan retorika keagamaan (tasawuf/Naqsyabandiyah) dengan perlawanan bersenjata dan memberi inspirasi pada generasi pemimpin berikutnya.",
    background: "/images/mansur-bg.jpeg",
    characterImage: "/images/mansur.png",
    avatarImage: "/images/mansur-avt.jpeg",
    contributions: [
      "Mengawali gelombang perlawanan religio-militer Kaukasus akhir abad ke-18",
      "Menyatukan jaringan sufi dan pejuang lokal untuk melawan pasukan Kekaisaran Rusia",
      "Menjadi figur simbolis bagi perlawanan berikutnya (termasuk Imam Shamil)"
    ]
  },
  {
    name: "Hadji Murad",
    period: "1818-1852 M",
    role: "Panglima Avar & Tokoh Perlawanan",
    description: "Panglima Avar yang terkenal karena kepandaian militer dan kisah hidupnya yang kemudian diabadikan (mis. oleh Leo Tolstoy). Ia berperan penting dalam konflik Dagestan melawan Rusia.",
    background: "/images/murad-bg.jpeg",
    characterImage: "/images/murad.png",
    avatarImage: "/images/murad-avt.jpeg",
    contributions: [
      "Pemimpin militer terkemuka dalam perjuangan Dagestan melawan Rusia",
      "Mengembangkan taktik gerilya di pegunungan Kaukasus",
      "Figur budaya-literer (disebutkan oleh Tolstoy) sehingga wajah/ceritanya mudah dicari"
    ]
  },
  {
    name: "Ismail Gasprinsky (Gaspirali)",
    period: "1851-1914 M",
    role: "Intelektual & Reformis (Jadid)",
    description: "Pemikir Crimean Tatar yang mendorong reformasi pendidikan dan modernisasi kaum Muslim Turkik di wilayah Kekaisaran Rusia — pengaruhnya merambah ke Asia Tengah dan Kaukasus melalui gerakan 'Jadid'.",
    background: "/images/ismail-bg.jpeg",
    characterImage: "/images/ismail.png",
    avatarImage: "/images/ismail-avt.jpg",
    contributions: [
      "Mendirikan surat kabar dan jaringan pendidikan modern untuk komunitas Muslim di Rusia",
      "Mengilhami gerakan Jadid di Asia Tengah yang mereformasi kurikulum agama dan sains",
      "Figur dengan foto & arsip tulisan yang mudah diakses"
    ]
  },
  {
    name: "Sayyid Mir Muhammad Alim Khan (Emir Alim Khan)",
    period: "1880-1944 M",
    role: "Emir terakhir Bukhara",
    description: "Penguasa terakhir Emirat Bukhara — tokoh penting akhir periode monarki Islam di Asia Tengah; foto-foto awal (Prokudin-Gorskii) tersedia sehingga wajahnya mudah ditemukan.",
    background: "/images/sayyid-bg.jpg",
    characterImage: "/images/sayyid.png",
    avatarImage: "/images/sayyid-avt.jpg",
    contributions: [
      "Memimpin Emirate of Bukhara sampai penggulingan 1920",
      "Simbol era terakhir pemerintahan Islam tradisional di Asia Tengah",
      "Fotografi warna awal (Prokudin-Gorskii) memudahkan pencarian wajah & arsip"
    ]
  },
  {
    name: "Said Afandi al-Chirkawi (Said Afandi)",
    period: "1937-2012 M",
    role: "Ulama Sufi & Murshid Naqshbandi",
    description: "Sufi murshid Dagestan yang sangat berpengaruh pada jamaah lokal dan regional; tokoh keagamaan modern dengan banyak foto & rekaman, wafat akibat serangan pada 2012.",
    background: "/images/said-bg.jpeg",
    characterImage: "/images/said.png",
    avatarImage: "/images/said-avt.jpeg",
    contributions: [
      "Pemimpin spiritual Naqshbandi di Dagestan dengan jaringan murid luas",
      "Mengorganisir majlis-majlis besar dan pendidikan sufistik modern",
      "Kehidupan dan peristiwa kematiannya terdokumentasi luas (media & jurnal lokal)"
    ]
  },
  {
    name: "Uzun-Hajji (Uzun Hajji)",
    period: "1848-1920 M",
    role: "Sheikh & Emir (North Caucasian Emirate)",
    description: "Pemimpin Naqshbandi yang menjadi Emir singkat North Caucasian Emirate (1919–1920) selama kekacauan Perang Saudara Rusia — tokoh agama-politik yang wajah/portrainya tersedia di arsip serta tulisan sejarah regional.",
    background: "/images/hajji-bg.jpg",
    characterImage: "/images/hajji.png",
    avatarImage: "/images/hajji-avt.jpg",
    contributions: [
      "Memproklamasikan dan memimpin North Caucasian Emirate pada 1919",
      "Mewakili gabungan peran keagamaan & politik pasca-Russian Revolution",
      "Relevan untuk studi Islam-politik di Kaukasus modern"
    ]
  }
]);


const selectHero = (index) => {
  if (currentHero.value !== index) {
    currentHero.value = index;
  }
};

// Heritage/Peninggalan Data
const heritages = ref([
  {
    name: "Masjid Juma Derbent",
    location: "Derbent, Dagestan, Rusia",
    year: "Abad ke-8 M (734 M)",
    description: "Salah satu masjid tertua di Rusia dan bekas wilayah Uni Soviet. Dibangun pada masa dinasti Umayyah dan masih berfungsi hingga kini.",
    image: "../images/peninggalan/derbent.jpg"
  },
  {
    name: "Benteng Derbent",
    location: "Derbent, Dagestan, Rusia",
    year: "Abad ke-6 M (difortifikasi Islam abad ke-8)",
    description: "Benteng kuno yang dijuluki 'Bab al-Abwab' (Gerbang Gerbang), menjadi pos penting pertahanan Islam di Kaukasus.",
    image: "../images/peninggalan/bentengnya.jpg"
  },
  {
    name: "Istana Shirvanshah",
    location: "Baku, Azerbaijan",
    year: "Abad ke-15 M",
    description: "Kompleks istana dinasti Shirvanshah yang menggabungkan arsitektur Islam Persia dengan elemen lokal Kaukasus.",
    image: "../images/peninggalan/shirvanshah.png"
  },
  {
    name: "Menara Maiden",
    location: "Baku, Azerbaijan",
    year: "Abad ke-12 M",
    description: "Menara ikonik di Old City Baku yang menjadi simbol arsitektur Islam Azerbaijan dan tercatat sebagai situs UNESCO.",
    image: "../images/peninggalan/maiden.jpg"
  },
  {
    name: "Masjid Bibi-Heybat",
    location: "Baku, Azerbaijan",
    year: "Abad ke-13 M (direkonstruksi 1990-an)",
    description: "Masjid bersejarah yang menjadi tempat ziarah penting di Azerbaijan, dikenal dengan kubah emasnya yang megah.",
    image: "../images/peninggalan/Masjid BibiHeybat.jpg"
  },
  {
    name: "Benteng Kala Quraysh",
    location: "Dagestan, Rusia",
    year: "Abad ke-7-8 M",
    description: "Benteng pertahanan Islam kuno di pegunungan Dagestan yang menjadi saksi perjuangan Muslim Kaukasus.",
    image: "../images/peninggalan/Benteng Kala Quraysh.jpg"
  },
  {
    name: "Masjid Agung Grozny",
    location: "Grozny, Chechnya",
    year: "2008 M",
    description: "Salah satu masjid terbesar di Eropa, dibangun sebagai simbol kebangkitan Islam Chechnya pasca perang.",
    image: "../images/peninggalan/Masjid Agung Grozny.jpg"
  },
  {
    name: "Makam Imam Shamil",
    location: "Gimry, Dagestan, Rusia",
    year: "1871 M",
    description: "Tempat pemakaman Imam Shamil yang menjadi situs ziarah penting bagi Muslim Kaukasus.",
    image: "../images/peninggalan/Makam Imam Shamil.jpg"
  },
  {
    name: "Masjid Taza Pir",
    location: "Baku, Azerbaijan",
    year: "Abad ke-14 M",
    description: "Masjid dan kompleks ziarah yang menggabungkan arsitektur Islam dengan tradisi spiritual lokal.",
    image: "../images/peninggalan/Masjid Taza Pir.png"
  }
]);

// FAQ Data
const openFAQ = ref(null);

const toggleFAQ = (index) => {
  openFAQ.value = openFAQ.value === index ? null : index;
};

const faqs = ref([
  {
    question: "Kapan Islam pertama kali masuk ke Kaukasus?",
    answer: "Islam pertama kali masuk ke Kaukasus pada abad ke-7 Masehi (sekitar tahun 640-660 M), tidak lama setelah wafatnya Nabi Muhammad ﷺ. Ekspedisi Arab pertama dipimpin oleh Abd al-Rahman ibn Rabi'ah pada masa Khilafah Rasyidun di bawah Khalifah Umar bin Khattab dan Utsman bin Affan."
  },
  {
    question: "Siapa tokoh paling terkenal dalam sejarah Islam Kaukasus?",
    answer: "Imam Shamil (1797-1871) adalah tokoh paling legendaris. Ia memimpin Imamat Kaukasus selama 25 tahun (1834-1859) dalam perlawanan melawan ekspansi Rusia, menyatukan berbagai suku Kaukasus, dan menerapkan sistem pemerintahan berdasarkan Syariah. Ia menjadi simbol perjuangan dan kemerdekaan bagi Muslim Kaukasus."
  },
  {
    question: "Apa peninggalan Islam tertua yang masih ada di Kaukasus?",
    answer: "Masjid Juma Derbent di Dagestan, Rusia, adalah salah satu peninggalan tertua, dibangun sekitar tahun 734 M (abad ke-8). Masjid ini merupakan salah satu masjid tertua di wilayah Rusia dan bekas Uni Soviet, dan masih berfungsi sebagai tempat ibadah hingga hari ini."
  },
  {
    question: "Bagaimana Islam bisa bertahan di era Soviet?",
    answer: "Meskipun menghadapi penindasan berat dari rezim komunis Soviet (penutupan masjid, larangan praktik keagamaan, penindasan ulama), Islam bertahan melalui praktik keagamaan dalam keluarga secara underground, hafalan Al-Quran yang diturunkan secara turun-temurun, dan jaringan tarekat sufi yang beroperasi secara rahasia."
  },
  {
    question: "Wilayah mana saja di Kaukasus yang mayoritas Muslim?",
    answer: "Wilayah dengan mayoritas Muslim di Kaukasus meliputi: Azerbaijan (sekitar 95%), Chechnya (96%), Dagestan (90%), Ingushetia (95%), dan Kabardino-Balkaria (70%). Wilayah-wilayah ini memiliki tradisi Islam yang kuat dan telah menjadi bagian integral dari identitas budaya mereka."
  },
  {
    question: "Apa peran tarekat sufi dalam sejarah Islam Kaukasus?",
    answer: "Tarekat sufi, terutama Naqsyabandiyah dan Qadiriyah, memainkan peran sangat penting dalam menjaga Islam di Kaukasus. Mereka tidak hanya menyebarkan ajaran spiritual, tetapi juga memimpin perlawanan melawan penjajah, membangun sistem pendidikan, dan menjaga kohesi sosial masyarakat Muslim Kaukasus."
  },
  {
    question: "Bagaimana kondisi Islam di Kaukasus saat ini?",
    answer: "Pasca runtuhnya Uni Soviet (1991), Islam mengalami kebangkitan signifikan di Kaukasus. Masjid dan madrasah dibangun kembali, generasi muda semakin sadar akan identitas Islam mereka, dan Islam menjadi bagian penting dari kehidupan politik dan budaya. Namun, wilayah ini juga menghadapi tantangan modernisasi dan konflik geopolitik."
  }
]);

// Sources Data
const sources = ref([
  "Zelkina, A. (2000). In Quest for God and Freedom: The Sufi Response to the Russian Advance in the North Caucasus. New York University Press.",
  "Gammer, M. (1994). Muslim Resistance to the Tsar: Shamil and the Conquest of Chechnia and Daghestan. Frank Cass Publishers.",
  "Bennigsen, A., & Wimbush, S. E. (1986). Muslims of the Soviet Empire: A Guide. Indiana University Press.",
  "UNESCO World Heritage Centre. Historic Centre of Derbent and Walled City of Baku.",
  "King, C. (2008). The Ghost of Freedom: A History of the Caucasus. Oxford University Press.",
  "Jersild, A. (2002). Orientalism and Empire: North Caucasus Mountain Peoples and the Georgian Frontier, 1845-1917. McGill-Queen's Press.",
  "Ware, R. B., & Kisriev, E. (2010). Dagestan: Russian Hegemony and Islamic Resistance in the North Caucasus. Routledge.",
  "Allen, W. E. D., & Muratoff, P. (1953). Caucasian Battlefields: A History of the Wars on the Turco-Caucasian Border. Cambridge University Press.",
  "Knysh, A. (2007). Sufism in the Caucasus. Journal of the History of Sufism.",
  "De Waal, T. (2010). The Caucasus: An Introduction. Oxford University Press."
]);

// Initialize on mount
onMounted(() => {
  typeEffect();
});

onUnmounted(() => {
  if (typingTimeout) {
    clearTimeout(typingTimeout);
  }
});
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}

.cursor {
  display: inline-block;
  margin-left: 4px;
  color: #92400e;
  font-weight: 300;
}

.cursor-blink {
  animation: blink 0.7s infinite;
}

@keyframes blink {
  0%, 50% {
    opacity: 1;
  }
  51%, 100% {
    opacity: 0;
  }
}

.typing-text {
  display: inline-block;
}

/* Hero Transition Animations */
.slide-up-enter-active,
.slide-up-leave-active {
  transition: all 0.6s ease;
}

.slide-up-enter-from {
  transform: translateY(100%);
  opacity: 0;
}

.slide-up-leave-to {
  transform: translateY(-100%);
  opacity: 0;
}

.slide-down-enter-active,
.slide-down-leave-active {
  transition: all 0.6s ease;
}

.slide-down-enter-from {
  transform: translateY(-100%);
  opacity: 0;
}

.slide-down-leave-to {
  transform: translateY(100%);
  opacity: 0;
}

/* Accordion Animation */
.accordion-enter-active,
.accordion-leave-active {
  transition: all 0.3s ease;
  overflow: hidden;
}

.accordion-enter-from,
.accordion-leave-to {
  max-height: 0;
  opacity: 0;
}

.accordion-enter-to,
.accordion-leave-from {
  max-height: 500px;
  opacity: 1;
}

/* Background Dissolve Transition */
.bg-dissolve-enter-active {
  animation: bgDissolve 1.2s ease-out;
}

.bg-dissolve-leave-active {
  animation: bgDissolve 0.8s ease-in reverse;
}

@keyframes bgDissolve {
  0% {
    opacity: 0;
    filter: blur(10px);
  }
  100% {
    opacity: 1;
    filter: blur(0);
  }
}

/* Character Show Up Transition */
.character-show-up-enter-active {
  animation: characterShowUp 1s ease-out;
}

.character-show-up-leave-active {
  animation: characterShowUp 0.6s ease-in reverse;
}

@keyframes characterShowUp {
  0% {
    opacity: 0;
    transform: translateY(100px) scale(0.8);
    filter: blur(8px);
  }
  60% {
    opacity: 1;
    filter: blur(0);
  }
  100% {
    opacity: 1;
    transform: translateY(0) scale(1);
    filter: blur(0);
  }
}

/* Slide Up Hero Transition */
.slide-up-hero-enter-active {
  animation: slideUpHero 0.8s ease-out;
}

.slide-up-hero-leave-active {
  animation: slideUpHero 0.5s ease-in reverse;
}

@keyframes slideUpHero {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ✨ Spotlight Beams — Soft Blending */
.spotlight-beam-center,
.spotlight-beam-left,
.spotlight-beam-right,
.spotlight-beam-pulse,
.spotlight-beam-fill-left,
.spotlight-beam-fill-right {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 100%;
  mix-blend-mode: screen;
  opacity: 0.5;
  pointer-events: none;
  transform-origin: bottom center;
  will-change: opacity, transform;
}

/* Center Beam */
.spotlight-beam-center {
  background: radial-gradient(
    ellipse at bottom,
    rgba(251, 191, 36, 0.55),
    rgba(251, 191, 36, 0.2) 40%,
    transparent 70%
  );
  filter: blur(24px);
  transform: scaleY(1.4);
}

/* Left Beam */
.spotlight-beam-left {
  background: radial-gradient(
    ellipse at bottom left,
    rgba(251, 146, 60, 0.45),
    rgba(251, 146, 60, 0.15) 40%,
    transparent 70%
  );
  filter: blur(26px);
  transform: rotate(-8deg) scaleY(1.3);
}

/* Right Beam */
.spotlight-beam-right {
  background: radial-gradient(
    ellipse at bottom right,
    rgba(250, 204, 21, 0.45),
    rgba(250, 204, 21, 0.15) 40%,
    transparent 70%
  );
  filter: blur(26px);
  transform: rotate(8deg) scaleY(1.3);
}

/* Pulsing beam */
.spotlight-beam-pulse {
  background: radial-gradient(
    ellipse at bottom,
    rgba(252, 211, 77, 0.4),
    rgba(252, 211, 77, 0.1) 40%,
    transparent 70%
  );
  filter: blur(30px);
  animation: spotlightPulse 3s ease-in-out infinite;
}

/* Fill beams for extra soft blending */
.spotlight-beam-fill-left,
.spotlight-beam-fill-right {
  background: radial-gradient(
    ellipse at bottom,
    rgba(255, 196, 92, 0.25),
    transparent 70%
  );
  filter: blur(40px);
}

/* Pulsation animation */
@keyframes spotlightPulse {
  0%, 100% {
    opacity: 0.45;
    transform: scaleY(1.3);
  }
  50% {
    opacity: 0.75;
    transform: scaleY(1.5);
  }
}

.character-image {
  filter: drop-shadow(0 25px 30px rgba(0, 0, 0, 0.6));
  border-radius: 1rem; /* tetap rounded */
}

.character-vignette {
  background: linear-gradient(to top, rgba(0, 0, 0, 0.25), transparent 60%);
}


.animate-float {
  animation: float 6s ease-in-out infinite;
}

.animate-float-delayed {
  animation: float 8s ease-in-out infinite;
  animation-delay: 1s;
}

.animate-float-slow {
  animation: float 10s ease-in-out infinite;
  animation-delay: 2s;
}

.animate-float-character {
  animation: floatCharacter 4s ease-in-out infinite;
}

@keyframes float {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-20px);
  }
}

@keyframes floatCharacter {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-15px);
  }
}

/* Pulse Animations */
.animate-pulse-slow {
  animation: pulseSlow 4s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

.animate-pulse-slower {
  animation: pulseSlow 6s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

.animate-pulse-spotlight {
  animation: pulseSpotlight 3s ease-in-out infinite;
}

.animate-pulse-delay-75 {
  animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
  animation-delay: 75ms;
}

.animate-pulse-delay-150 {
  animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
  animation-delay: 150ms;
}

@keyframes pulseSlow {
  0%, 100% {
    opacity: 0.3;
  }
  50% {
    opacity: 0.8;
  }
}

@keyframes pulseSpotlight {
  0%, 100% {
    opacity: 0.6;
  }
  50% {
    opacity: 1;
  }
}

/* Spin Animation */
.animate-spin-very-slow {
  animation: spin 30s linear infinite;
}

@keyframes spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

/* Radial Gradient Utility */
.bg-gradient-radial {
  background: radial-gradient(circle, var(--tw-gradient-stops));
}

/* Smooth Scroll */
@media (prefers-reduced-motion: no-preference) {
  html {
    scroll-behavior: smooth;
  }
}
</style>