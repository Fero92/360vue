<template>
    <section class="features-grid py-16 bg-gray-100">
      <div class="container mx-auto px-4">
        <h2 class="text-2xl md:text-3xl font-bold text-center mb-12">{{ title }}</h2>
        
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <div v-for="feature in features" :key="feature.id" class="features-grid__card bg-white p-6 rounded-lg shadow-md flex items-start hover:shadow-lg transition duration-300">
            <div class="features-grid__icon bg-teal-100 w-12 h-12 rounded-full flex items-center justify-center mr-4 flex-shrink-0">
              <img :src="feature.icon" alt="Feature icon" class="h-5 w-5" />
            </div>
            <div>
              <h3 class="text-lg font-semibold mb-2">{{ feature.title }}</h3>
              <p class="text-gray-600 text-sm">{{ feature.description }}</p>
              <a v-if="feature.link" :href="feature.link" class="inline-block mt-3 text-teal-600 text-sm font-medium hover:text-teal-700">
                {{ feature.linkText }}
              </a>
            </div>
          </div>
        </div>
        
        <div class="text-center mt-10">
          <a href="#" class="inline-block border-2 border-teal-600 text-teal-600 px-6 py-2 rounded-lg font-medium hover:bg-teal-600 hover:text-white transition duration-200">
            {{ mainCta }}
          </a>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'FeaturesGrid',
    data() {
      return {
        title: 'Profesionálne bankovníctvo v banke, v ktorej je financovanie revolučné',
        mainCta: 'Zobraziť všetky služby',
        features: [
          {
            id: 1,
            title: 'Bezplatné vedenie účtu',
            description: 'Bez zbytočných poplatkov za vedenie účtu, výbery z bankomatov a základné služby. Všetko bez podmienok.',
            icon: '@/assets/icons/account.svg',
            link: '#',
            linkText: 'Otvoriť účet'
          },
          {
            id: 2,
            title: 'Okamžité platby',
            description: 'Peniaze odoslané v rámci Slovenska či do eurozóny dôjdu k príjemcovi v priebehu niekoľkých sekúnd.',
            icon: '@/assets/icons/payment.svg',
            link: '#',
            linkText: 'Viac o platbách'
          },
          {
            id: 3,
            title: 'Platby mobilom',
            description: 'Zaplatíte aj bez fyzickej karty - stačí vám smartfón s NFC a naša aplikácia. Podporujeme Apple Pay aj Google Pay.',
            icon: '@/assets/icons/mobile-pay.svg',
            link: '#',
            linkText: 'Aktivovať platby mobilom'
          },
          {
            id: 4,
            title: 'Výhodné investovanie',
            description: 'Zhodnocujte svoje úspory vďaka našim investičným produktom s atraktívnymi výnosmi aj pre začiatočníkov.',
            icon: '@/assets/icons/invest.svg',
            link: '#',
            linkText: 'Začať investovať'
          }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  /* BEM methodology for any custom styling */
  .features-grid__card {
    transition: all 0.3s ease;
  }
  .features-grid__card:hover .features-grid__icon {
    background-color: #e6fffa;
  }
  </style>