<template>
    <header class="bg-white shadow-sm">
      <div class="container mx-auto px-4 py-2">
        <div class="flex items-center justify-between">
          <!-- Logo -->
          <div class="logo">
            <router-link to="/" class="flex items-center">
              <img :src="ucetBoxPng" alt="365.bank" class="h-8" />
            </router-link>
          </div>
          
          <!-- Navigation - Desktop -->
          <nav class="hidden md:flex space-x-6">
            <a v-for="item in navItems" 
               :key="item.id" 
               :href="item.url" 
               class="text-gray-700 hover:text-teal-500 transition duration-200">
              {{ item.label }}
            </a>
          </nav>
          
          <!-- Action Buttons -->
          <div class="flex items-center space-x-2">
            <button class="font-medium bg-[#45dbcc] text-white px-4 py-2 rounded-full text-sm h-[50px] border-2 border-[#45dbcc] hover:bg-white hover:text-[#004155] hover:border-[bg-white] transition duration-100 ease-in-out">
              {{ actionButtons.primary }}
            </button>
            
            <button class="border border-gray-300 text-gray-700 px-4 py-2 rounded text-sm flex items-center">
              {{ actionButtons.secondary }}
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
              </svg>
            </button>
            
            

            <!-- Search -->
            <button class="text-gray-500 hover:text-gray-700 md:ml-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
              </svg>
            </button>
            
            <!-- Mobile Menu Button -->
            <button @click="toggleMobileMenu" class="md:hidden text-gray-500 hover:text-gray-700">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path v-if="mobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
              </svg>
            </button>
          </div>
        </div>
        
        <!-- Mobile Navigation Menu -->
        <div v-if="mobileMenuOpen" class="md:hidden mt-4 pb-4">
          <nav class="mobile-nav flex flex-col space-y-3">
            <a v-for="item in navItems" 
               :key="item.id" 
               :href="item.url" 
               class="text-gray-700 hover:text-teal-500 transition duration-200 py-2 border-b border-gray-100">
              {{ item.label }}
            </a>
          </nav>
        </div>
      </div>
    </header>
  </template>
  
  <script>
  import ucetBoxPng from '@/assets/ucet-box.png';
  
  export default {
    name: 'TheHeader',
    data() {
      return {
        mobileMenuOpen: false,
        navItems: [
          { id: 1, label: 'E-kon produktový', url: '#' },
          { id: 2, label: 'Úvery a pôžičky', url: '#' },
          { id: 3, label: 'Mobilný banking', url: '#' },
          { id: 4, label: 'Sporenie a investovanie', url: '#' },
          { id: 5, label: 'Poistenie', url: '#' },
          { id: 6, label: 'O nás', url: '#' }
        ],
        actionButtons: {
          primary: 'Bankova karta',
          secondary: 'Internet banking'
        }
      }
    },
    methods: {
      toggleMobileMenu() {
        this.mobileMenuOpen = !this.mobileMenuOpen
      }
    }
  }
  </script>
  
  <style scoped>
  /* Using BEM methodology for any custom styling */
  .logo {
    /* BEM example for logo styling */
  }
  .logo__image {
    /* BEM modifier if needed */
  }
  </style>