<template>
  <div
    class="flex flex-col items-center justify-between bg-white px-8 py-2 lg:flex-row"
  >
    <quasiaiLogo />

    <ul class="flex flex-col items-center gap-4 lg:flex-row">
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
