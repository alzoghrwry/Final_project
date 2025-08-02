<template>
  <li class="w-full md:w-auto">
    <router-link
      :to="href"
      class="hover:text-primary dark:text-white dark:hover:text-blue-300 text-lg w-full block py-2"
    >
      {{ label }}
    </router-link>
  </li>
</template>

<script setup>
defineProps({
  href: {
    type: String,
    default: '/'
  },
  label: {
    type: String,
    required: true
  }
})
</script>
