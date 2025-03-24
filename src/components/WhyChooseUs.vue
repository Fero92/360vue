<template>
    <section class="why-choose bg-white py-16">
      <div class="container mx-auto px-4">
        <h2 class="text-2xl md:text-3xl font-bold text-center mb-12">{{ title }}</h2>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          <div v-for="reason in reasons" :key="reason.id" class="why-choose__card text-center p-6 rounded-lg border border-gray-100 hover:shadow-lg transition duration-300">
            <div class="why-choose__icon bg-teal-50 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
              <img :src="reason.icon" alt="Feature icon" class="h-8 w-8" />
            </div>
            <h3 class="text-lg font-semibold mb-3">{{ reason.title }}</h3>
            <p class="text-gray-600 text-sm">{{ reason.description }}</p>
            
            <a v-if="reason.link" :href="reason.link" class="inline-block mt-4 text-teal-600 text-sm font-medium hover:text-teal-700">
              {{ reason.linkText }}
            </a>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'WhyChooseUs',
    data() {
      return {
        title: 'Prečo práve 365-ka?',
        reasons: [
          {
            id: 1,
            title: 'TRANSPARENTNOSŤ',
            description: 'Vždy viete na čom ste, nič vám nezatajíme. Jasné poplatky, všetko účtujeme.',
            icon: '@/assets/icons/transparency.svg',
            link: '#',
            linkText: 'Viac informácií'
          },
          {
            id: 2,
            title: 'DIGITÁLNA BANKA',
            description: 'Pohodlne, rýchlo a bez papieru. Zo smartfónu. Po otvorenie províziu.',
            icon: '@/assets/icons/digital.svg',
            link: '#',
            linkText: 'Ako nás využívať'
          },
          {
            id: 3,
            title: 'FÉROVÝ PRÍSTUP ZADARMO',
            description: 'Možnosti k bankovaniu k nemu trehne zadankami sporabni, len aj zápletí sporejsne k trnám.',
            icon: '@/assets/icons/fairness.svg',
            link: '#',
            linkText: 'Zozrieť ponuku'
          },
          {
            id: 4,
            title: 'MOBILNÁ APPLIKÁCIA',
            description: 'Vybavíte si 100% účetu na mobilu, výnijnka s nolokým o návsane vyničžená v celkomy smiete, či loute.',
            icon: '@/assets/icons/mobile-app.svg',
            link: '#',
            linkText: 'Získať si apku'
          }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  /* BEM methodology for any custom styling */
  .why-choose__card {
    transition: all 0.3s ease;
  }
  .why-choose__card:hover .why-choose__icon {
    background-color: #e6fffa;
  }
  </style>