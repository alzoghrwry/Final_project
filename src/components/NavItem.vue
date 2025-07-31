<script setup>
defineProps({
  href: String,
  label: String
})
</script>

<template>
  <router-link
    :to="href"
    class="block w-full text-right text-primary dark:text-white hover:underline"
  >
    {{ label }}
  </router-link>
</template>
