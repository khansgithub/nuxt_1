<template>
  <div>
    <NuxtLayout>
       <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<script setup lang="ts">
import '~/assets/main.css'
useHead({
  bodyAttrs: {
    "data-bs-theme": 'dark'
  }
})
</script>