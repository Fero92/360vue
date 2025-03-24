<template>
    <section class="card-section py-16 bg-gray-50">
      <div class="container mx-auto px-4">
        <div class="flex flex-col md:flex-row items-center justify-between">
          <div class="card-section__image md:w-2/5 mb-10 md:mb-0">
            <img src="@/assets/ucet-box.png" alt="Bank card" class="w-full max-w-md mx-auto" />
          </div>
          <div class="card-section__content md:w-3/5 md:pl-12">
            <h2 class="text-2xl md:text-3xl font-bold mb-6">{{ card.title }}</h2>
            <p class="text-gray-700 mb-8">{{ card.description }}</p>
            
            <ul class="card-section__features space-y-4 mb-8">
              <li v-for="(feature, index) in card.features" :key="index" class="flex items-start">
                <svg class="h-6 w-6 text-teal-500 mr-3 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                <span>{{ feature }}</span>
              </li>
            </ul>
            
            <a href="#" class="inline-block bg-teal-500 text-white px-6 py-3 rounded-lg font-medium hover:bg-teal-600 transition duration-200">
              {{ card.cta }}
            </a>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'CardSection',
    data() {
      return {
        card: {
          title: 'Stiahni si apku a staň sa súčasťou 365.bank',
          description: 'Bližšia borušn vidieť znovu sa tropu naúčaľa z pležitievať v nostlia ryžbiaté. Tie oj a predať a pre smetá sa azaké ičpaté poriadky, sprovor si došlo...',
          features: [
            'Jednoduchá správa tvojich financií',
            'Nonstop prístup k účtu odkiaľkoľvek',
            'Rýchle platby a prevody',
            'Prístup ku všetkým produktom banky'
          ],
          cta: 'Stiahni si aplikáciu z obchodov'
        }
      }
    }
  }
  </script>
  
  <style scoped>
  /* BEM methodology for custom styling */
  .card-section__image img {
    filter: drop-shadow(0 10px 15px rgba(0, 0, 0, 0.1));
  }
  .card-section__features li {
    transition: transform 0.2s ease;
  }
  .card-section__features li:hover {
    transform: translateX(4px);
  }
  </style>