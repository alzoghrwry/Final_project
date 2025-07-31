<script setup>
import { ref } from 'vue'
import NavItem from '@/components/NavItem.vue'
import DropdownNav from '@/components/DropdownNav.vue'

const isMenuOpen = ref(false)
const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
const closeMenu = () => {
  isMenuOpen.value = false
}
</script>

<template>
  <header class="relative z-50 w-full">

    <div class="flex justify-end md:hidden p-4">
      <button @click="toggleMenu" class="text-2xl text-primary dark:text-white">
        <i class="fas fa-bars"></i>
      </button>
    </div>

   
    <div v-if="isMenuOpen" class="fixed right-0 left-4  inset-0 bg-white opacity-75 dark:bg-gray-900 z-50 flex flex-col  p-6 md:hidden" >
     
      <div class="flex justify-end ml-6">
        <button @click="closeMenu" class="text-3xl text-primary dark:text-white">
          <i class="fas fa-times"></i>
        </button>
      </div>

      
     <div class="mt-8 space-y-6 text-lg">
  <NavItem @click="closeMenu" href="/" label="الرئيسية" />
  <NavItem @click="closeMenu" href="/view/About" label="مسام" />
  <NavItem @click="closeMenu" href="/view/News" label="الأخبار" />
  <NavItem @click="closeMenu" href="/view/Story" label="قصص النجاح" />

  <DropdownNav
    @click="closeMenu"
    label="إعلام مسام"
    :items="[
      { label: 'الفيديوهات', href: '/media/videos' },
      { label: 'الصور', href: '/media/images' },
      { label: 'قصص النجاح', href: '/view/Story' }
    ]"
  />

  <NavItem @click="closeMenu" href="/contact" label="تواصل معنا" />
</div>


      <!-- البحث -->
      <div class="mt-8">
        <div class="flex items-center border border-gray-300 dark:border-gray-600 rounded px-3 py-2 bg-white dark:bg-gray-700">
          <i class="fas fa-search text-gray-500 dark:text-white"></i>
          <input type="text" placeholder="ابحث هنا" class="bg-transparent focus:outline-none w-full text-sm mr-2">
        </div>
      </div>
    </div>

   
    <nav class="hidden md:flex gap-8 items-center">
      <NavItem href="/" label="الرئيسية" />
      <NavItem href="/view/About" label="مسام" />
      <NavItem href="/view/News" label="الأخبار" />
      <NavItem href="/view/Story" label="قصص النجاح" />
      <DropdownNav
        label="إعلام مسام"
        :items="[
          { label: 'الفيديوهات', href: '#' },
          { label: 'الصور', href: '#' },
          { label: 'قصص النجاح', href: '#' }
        ]"
      />
      <NavItem label="تواصل معنا" />
      <div class="flex items-center border border-gray-300 dark:border-gray-600 rounded px-3 py-2 bg-white dark:bg-gray-700">
        <i class="fas fa-search text-gray-500 dark:text-white"></i>
        <input type="text" placeholder="ابحث هنا" class="bg-transparent focus:outline-none w-full text-sm mr-2">
      </div>
    </nav>
  </header>
</template>
