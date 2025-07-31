<template>
  <div class="grid grid-rows-[auto_auto_auto_1fr_auto] h-full">
    <Header />
    <HeroSection />
    <Contact />
    <Footer />
  </div>
</template>

<script setup>
import Header from '@/components/Header.vue'
import HeroSection from '@/components/HeroSection.vue'
import Contact from '@/components/Contact.vue'
import Footer from '@/components/Footer.vue'
</script>