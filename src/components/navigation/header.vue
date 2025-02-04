<template>
  <div class="flex items-center justify-between bg-white px-8 py-2">
    <quasiaiLogo />

    <ul class="flex space-x-8">
      <li>Features</li>
      <li>How it works</li>
      <li>Pricing</li>
      <NuxtLink to="/auth/login"
        ><UButton color="cyan">Get Started</UButton></NuxtLink
      >
    </ul>
  </div>
</template>

<script setup>
import quasiaiLogo from '~/assets/media/svgs/quasiai-logo.vue'
</script>
