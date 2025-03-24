<template>
    <footer class="bg-teal-800 text-white pt-12 pb-6">
      <div class="container mx-auto px-4">
        <!-- Footer Navigation -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 gap-8 mb-12">
          <!-- Contact -->
          <div class="footer__section">
            <h3 class="text-lg font-semibold mb-4">{{ sections.contact.title }}</h3>
            <div class="footer__contact mb-4">
              <div class="text-2xl font-bold">{{ sections.contact.phone }}</div>
              <div class="text-sm text-teal-200">{{ sections.contact.hours }}</div>
            </div>
            <div class="footer__links space-y-2">
              <a v-for="(link, index) in sections.contact.links" :key="index" href="#" class="block text-teal-200 hover:text-white transition">
                {{ link }}
              </a>
            </div>
          </div>
          
          <!-- Other Sections -->
          <div v-for="(section, key) in sections.main" :key="key" class="footer__section">
            <h3 class="text-lg font-semibold mb-4">{{ section.title }}</h3>
            <ul class="footer__links space-y-2">
              <li v-for="(link, index) in section.links" :key="index">
                <a href="#" class="text-teal-200 hover:text-white transition">{{ link }}</a>
              </li>
            </ul>
          </div>
        </div>
        
        <!-- Social and Apps -->
        <div class="flex flex-col md:flex-row justify-between items-center border-t border-teal-700 pt-8 mb-8">
          <div class="footer__social flex space-x-4 mb-6 md:mb-0">
            <a v-for="(social, key) in socials" :key="key" href="#" class="text-white hover:text-teal-200 transition">
              <i :class="social.icon"></i>
              {{ social.name }}
            </a>
          </div>
          
          <div class="footer__apps flex space-x-4">
            <a href="#" class="bg-white text-teal-800 px-4 py-2 rounded-lg flex items-center">
              <svg class="h-5 w-5 mr-2" fill="currentColor" viewBox="0 0 20 20">
                <path d="M10 0C4.477 0 0 4.477 0 10c0 5.523 4.477 10 10 10 5.523 0 10-4.477 10-10C20 4.477 15.523 0 10 0zm0 18c-4.418 0-8-3.582-8-8s3.582-8 8-8 8 3.582 8 8-3.582 8-8 8z"/>
              </svg>
              App Store
            </a>
            <a href="#" class="bg-white text-teal-800 px-4 py-2 rounded-lg flex items-center">
              <svg class="h-5 w-5 mr-2" fill="currentColor" viewBox="0 0 20 20">
                <path d="M10 0C4.477 0 0 4.477 0 10c0 5.523 4.477 10 10 10 5.523 0 10-4.477 10-10C20 4.477 15.523 0 10 0zm0 18c-4.418 0-8-3.582-8-8s3.582-8 8-8 8 3.582 8 8-3.582 8-8 8z"/>
              </svg>
              Google Play
            </a>
          </div>
        </div>
        
        <!-- Copyright -->
        <div class="footer__copyright border-t border-teal-700 pt-6 text-sm text-teal-200">
          <div class="flex flex-col md:flex-row justify-between">
            <p>© 2023 365.bank a.s.</p>
            <div class="footer__legal flex flex-wrap gap-x-4 gap-y-2 mt-2 md:mt-0">
              <a href="#" class="hover:text-white transition">365 INTERNATIONAL LIMITED</a>
              <a href="#" class="hover:text-white transition">COOKIES POLICY & NOTICE</a>
              <a href="#" class="hover:text-white transition">PRIVACY POLICY</a>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'TheFooter',
    data() {
      return {
        sections: {
          contact: {
            title: 'Kontaktujte nás',
            phone: '0850 365 365',
            hours: 'Dostupné 8:00-20:00',
            links: [
              'Nájsť pobočku',
              'Kontaktný formulár',
              'Napísať e-mail',
              'Callback service'
            ]
          },
          main: {
            products: {
              title: 'Pre vašu domácnosť',
              links: [
                'Účty a balíčky',
                'Pôžičky',
                'Hypotéky',
                'Sporenie',
                'Termínované vklady',
                'Poistenie',
                'Investovanie',
                'Bankové poplátky'
              ]
            },
            services: {
              title: 'Digitálne služby',
              links: [
                'Internetové bankovníctvo',
                'Mobilné bankovníctvo',
                'Online platby',
                'Virtual banking system',
                'Osobný účet',
                'Karta a doplnky',
                'Kurzový lístok'
              ]
            },
            support: {
              title: 'Užitočné odkazy',
              links: [
                'Často kladené otázky',
                'Návody a tipy',
                'Bezpečnosť online',
                'Reklamácie',
                'Blog',
                'Kariéra',
                'Tlačové správy'
              ]
            },
            about: {
              title: 'O nás',
              links: [
                'Profil',
                'História',
                'Riadiace orgány',
                'Stratégia a hodnoty',
                'Správy',
                'Ochrana údajov',
                'Distribúcia',
                'Pre médiá'
              ]
            }
          }
        },
        socials: {
          facebook: { name: 'Facebook', icon: 'fab fa-facebook-f' },
          instagram: { name: 'Instagram', icon: 'fab fa-instagram' },
          linkedin: { name: 'LinkedIn', icon: 'fab fa-linkedin-in' }
        }
      }
    }
  }
  </script>
  
  <style scoped>
  /* BEM methodology for any custom styling */
  .footer__section {
    /* Custom styling */
  }
  .footer__links a {
    transition: color 0.2s ease;
  }
  .footer__social a {
    transition: color 0.2s ease;
  }
  .footer__apps a {
    transition: all 0.3s ease;
  }
  .footer__apps a:hover {
    background-color: #f8f8f8;
  }
  </style>