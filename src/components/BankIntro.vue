<template>
    <section class="bank-intro py-16 bg-white">
      <div class="container mx-auto px-4 text-center">
        <h2 class="text-2xl md:text-3xl font-bold mb-3">{{ title }}</h2>
        <h3 class="text-xl text-teal-600 font-semibold mb-8">{{ subtitle }}</h3>
        
        <p class="max-w-2xl mx-auto text-gray-700 mb-8">
          {{ description }}
        </p>
        
        <div class="bank-intro__features flex flex-col md:flex-row md:justify-center space-y-8 md:space-y-0 md:space-x-8">
          <div v-for="feature in features" :key="feature.id" class="bank-intro__feature bg-white rounded-lg shadow-lg p-6 transform transition duration-300 hover:-translate-y-1 hover:shadow-xl">
            <div class="bg-gradient-to-r from-teal-500 to-teal-600 w-12 h-12 rounded-full flex items-center justify-center mx-auto mb-4">
              <img :src="feature.icon" alt="Feature icon" class="h-6 w-6" />
            </div>
            <h4 class="text-lg font-semibold mb-2">{{ feature.title }}</h4>
            <p class="text-gray-600 text-sm">{{ feature.description }}</p>
            <a :href="feature.link" class="block mt-4 text-teal-600 font-medium hover:text-teal-700">
              {{ feature.linkText }}
            </a>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'BankIntro',
    data() {
      return {
        title: 'Ahoj, sme 365.bank',
        subtitle: 'A chceme byť tvoja banka',
        description: 'Dobrolý uplatniať, oslaď? No, či poznáte cesty, ovom banka, ktorú každý kordík. Ulie vedieť ľen, abý vyhľa často nfelo sa peniaze najprv, otravný. Aban, áj by to. Co pre dobro hrmota? Poskrúcaj, ktoréé móžete priťahovať veľo so kobo na úside.',
        features: [
          {
            id: 1,
            title: 'APP',
            description: 'Naše mobilné aplikace zadarmo radení a Prehľad roztpeňov v bohatstvým vyplatenie v moiblnom aplikaci',
            icon: '@/assets/icons/mobile.svg',
            link: '#',
            linkText: 'Viac info'
          },
          {
            id: 2,
            title: 'INTERNET BANKING',
            description: 'Pohlaď ať som, tak že v cennovat mnietá v aplikačné cestám. Navečáj položky, ktoré si dám chovaniť vyhľáda. Zmienok za stránok a všetko.',
            icon: '@/assets/icons/laptop.svg',
            link: '#',
            linkText: 'Zistite viac'
          },
          {
            id: 3,
            title: 'BANKING MOBILE',
            description: 'Už teď možno pokročit mobilů cvok také. Máme roštýling finančne kontrole pomůže zistiac je také našim vyháľno s časie.',
            icon: '@/assets/icons/smartphone.svg',
            link: '#',
            linkText: 'Zistite viac o mobile'
          }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  /* BEM methodology for any custom styling */
  .bank-intro__feature {
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  </style>