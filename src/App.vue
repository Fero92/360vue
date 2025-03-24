<template>
  <div class="min-h-screen flex flex-col">
    <!-- Header -->
    <TheHeader />
    
    <!-- Main Content -->
    <main class="flex-grow">
      <!-- Hero Banner -->
      <HeroBanner />
      
      <!-- Bank Introduction -->
      <BankIntro />
      
      <!-- Features Grid -->
      <FeaturesGrid />
      
      <!-- Exchange Rates -->
      <ExchangeRates />
      
      <!-- Card Section -->
      <CardSection />
      
      <!-- Why Choose Us -->
      <WhyChooseUs />
      
      <!-- Latest Articles -->
      <LatestArticles />
    </main>
    
    <!-- Footer -->
    <TheFooter />
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue'
import HeroBanner from './components/HeroBanner.vue'
import BankIntro from './components/BankIntro.vue'
import FeaturesGrid from './components/FeaturesGrid.vue'
import ExchangeRates from './components/ExchangeRates.vue'
import CardSection from './components/CardSection.vue'
import WhyChooseUs from './components/WhyChooseUs.vue'
import LatestArticles from './components/LatestArticles.vue'
import TheFooter from './components/TheFooter.vue'

export default {
  name: 'App',
  components: {
    TheHeader,
    HeroBanner,
    BankIntro,
    FeaturesGrid,
    ExchangeRates,
    CardSection,
    WhyChooseUs,
    LatestArticles,
    TheFooter
  }
}
</script>