<template>
    <section class="hero bg-[#004155] text-white py-16">
      <div class="container mx-auto px-4">
        <div class="flex flex-col md:flex-row items-center justify-between">
          <div class="hero__content md:w-1/2 mb-10 md:mb-0">
            <div class="text-4xl font-medium inline-block bg-[#45dbcc] text-[#004155] px-3 py-1 rounded mb-4">
              {{ banner.tag }}
            </div>
            <h1 class="text-3xl md:text-xl font-light mb-4">{{ banner.title }}</h1>
            <p class="text-xl font-light mb-6">{{ banner.description }}</p>
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
          title: 'Čo sa váľa, to nezarába. V časoch rastúcich cien netreba hromadiť peniaze pod vankúšom. Ulož si ich radšej na Termínovaný vklad so zvýhodneným úrokom až 3 % ročne. Stačí si dohodnúť stretnutie v 365 pobočke. Ideš do toho?',
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