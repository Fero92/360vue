<template>
    <section class="exchange-rates bg-teal-800 py-12">
      <div class="container mx-auto px-4">
        <h2 class="text-2xl text-white font-bold text-center mb-8">{{ title }}</h2>
        
        <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
          <div v-for="rate in rates" :key="rate.pair" class="exchange-rates__card bg-teal-700 p-4 rounded-lg">
            <div class="flex justify-between items-center mb-2">
              <span class="text-white font-medium">{{ rate.pair }}</span>
              <span :class="{'text-green-400': rate.change > 0, 'text-red-400': rate.change < 0, 'text-gray-300': rate.change === 0}">
                {{ rate.change > 0 ? '+' + rate.change : rate.change }}
              </span>
            </div>
            <div class="text-white text-xl font-bold">{{ rate.value }}</div>
          </div>
        </div>
        
        <div class="text-center mt-6">
          <p class="text-teal-200 text-sm">{{ ratesInfo }}</p>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'ExchangeRates',
    data() {
      return {
        title: 'Aktuálne výmenné kurzy',
        ratesInfo: 'Ceny menový aktualizované k 10:00',
        rates: [
          { pair: 'EUR/USD', value: '1.071', change: 0.003 },
          { pair: 'EUR/GBP', value: '0.851', change: -0.002 },
          { pair: 'EUR/CZK', value: '25.345', change: 0.145 },
          { pair: 'EUR/PLN', value: '4.322', change: 0.001 },
          { pair: 'USD/JPY', value: '150.732', change: 0.532 },
          { pair: 'GBP/USD', value: '1.259', change: 0.007 },
          { pair: 'CHF/EUR', value: '0.923', change: -0.004 },
          { pair: 'AUD/USD', value: '0.671', change: 0.002 }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  /* BEM methodology for any custom styling */
  .exchange-rates__card {
    transition: transform 0.2s ease;
  }
  .exchange-rates__card:hover {
    transform: translateY(-2px);
  }
  </style>