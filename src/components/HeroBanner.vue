<template>
    <section class="hero bg-teal-800 text-white py-16">
      <div class="container mx-auto px-4">
        <div class="flex flex-col md:flex-row items-center justify-between">
          <div class="hero__content md:w-1/2 mb-10 md:mb-0">
            <div class="text-4xl font-medium inline-block bg-[#45dbcc] text-[#004155] px-3 py-1 rounded mb-4">
              {{ banner.tag }}
            </div>
            <h1 class="text-3xl md:text-4xl font-bold mb-4">{{ banner.title }}</h1>
            <p class="text-lg mb-6">{{ banner.description }}</p>
            <a href="#" class="hero__button bg-white text-teal-800 px-6 py-3 rounded-full font-medium hover:bg-gray-100 transition duration-200">
              {{ banner.cta }}
              <span class="ml-2">→</span>
            </a>
          </div>
          <div class="hero__image md:w-1/2">
            <img src="@/assets/ucet-box.png" alt="Banking illustration" class="w-full max-w-md mx-auto" />
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'HeroBanner',
    data() {
      return {
        banner: {
          tag: 'Zarábaj s úrokom až 3 % ročne',
          title: 'Čo to vášk v nadpisoch nie je? Iba kvalitné Zarábaj s úrokom až 3 % ročne. Odkiaľ pochádajú, výhoda ako žiaden',
          description: 'Staň si skutočným partnerom v 365 poistenia. Viac do 10:00?',
          cta: 'Zisti viac'
        }
      }
    }
  }
  </script>
  
  <style scoped>
  /* BEM methodology for custom styling */
  .hero__content {
    /* Custom styling */
  }
  .hero__image {
    /* Custom styling */
  }
  .hero__button {
    /* Custom styling */
  }
  </style>