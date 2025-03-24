<template>
    <section class="articles bg-gray-50 py-16">
      <div class="container mx-auto px-4">
        <div class="flex justify-between items-center mb-8">
          <h2 class="text-2xl md:text-3xl font-bold">{{ title }}</h2>
          <a href="#" class="text-teal-600 hover:text-teal-700 font-medium flex items-center">
            {{ moreLink }}
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
            </svg>
          </a>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div v-for="article in articles" :key="article.id" class="articles__card bg-white rounded-lg overflow-hidden shadow-md hover:shadow-lg transition duration-300">
            <div class="articles__image h-48 overflow-hidden">
              <img :src="article.image" :alt="article.title" class="w-full h-full object-cover transition duration-300 transform hover:scale-105" />
            </div>
            <div class="p-6">
              <div class="text-sm text-gray-500 mb-2">{{ article.date }}</div>
              <h3 class="text-lg font-semibold mb-3">{{ article.title }}</h3>
              <p class="text-gray-600 text-sm mb-4">{{ article.excerpt }}</p>
              <a :href="article.link" class="text-teal-600 hover:text-teal-700 font-medium text-sm">
                {{ article.linkText }}
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'LatestArticles',
    data() {
      return {
        title: 'Najnovšie články',
        moreLink: 'Viac',
        articles: [
          {
            id: 1,
            title: 'Ako si správne založiť finančnú rezervu?',
            excerpt: 'Tvoje peniaze určvane dožitý sati rán z chaty. Pokto, a pripadovéj šibo, viac máte, fó nať reč...',
            date: '15 Marec 2023',
            image: '@/assets/articles/article1.jpg',
            link: '#',
            linkText: 'Čítať viac'
          },
          {
            id: 2,
            title: 'Chceš byť po rozmilovaní tým, ako sú tvoje deti?',
            excerpt: 'Napojit sa v zložeň finančný? Pretea vám ach čilg, Evina Loďorlá, Parc propetam.',
            date: '3 Marec 2023',
            image: '@/assets/articles/article2.jpg',
            link: '#',
            linkText: 'Čítať viac'
          },
          {
            id: 3,
            title: 'Tvorba by mala domova realizovať',
            excerpt: 'Naozraj, z radšei spordačný pouzeš ra hĺbky ladnej, z viete aj opordačé veladinúd váže (vňedé na ❤️)',
            date: '28 Február 2023',
            image: '@/assets/articles/article3.jpg',
            link: '#',
            linkText: 'Čítať viac'
          }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  /* BEM methodology for any custom styling */
  .articles__card {
    transition: all 0.3s ease;
  }
  .articles__image {
    overflow: hidden;
  }
  .articles__image img {
    transition: transform 0.5s ease;
  }
  </style>