
<template>
  <div class="grid grid-rows-[auto_auto_auto_1fr_auto] h-full">
    <Header />
    <Topbar />
    <ProjectStats/>
    <Contact />
    <Footer />
  </div>
</template>

<script setup>
import Header from '@/components/Header.vue'
import Topbar from '@/components/Topbar.vue'
import Contact from '@/components/Contact.vue'
import Footer from '@/components/Footer.vue'
import ProjectStats from '@/components/ProjectStats.vue'
</script>
