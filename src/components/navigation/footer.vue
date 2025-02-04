<template>
  <div class="flex items-center justify-between bg-[#C6E6F3] px-8 py-6">
    <quasiaiLogo />

    <ul class="flex space-x-2">
      <OkSocial />
      <VkSocial />
      <TelegramSocial />
      <FacebookSocial />
      <Instagram />

      <p class="pl-6 text-sm">© 2025 - Copyright <br />All rights reserved</p>
    </ul>
  </div>
</template>

<script setup>
import FacebookSocial from '~/assets/media/svgs/social/facebook-social.vue'
import Instagram from '~/assets/media/svgs/social/instagram.vue'
import OkSocial from '~/assets/media/svgs/social/ok-social.vue'
import VkSocial from '~/assets/media/svgs/social/vk-social.vue'
import TelegramSocial from '~/assets/media/svgs/social/telegram-social.vue'
import quasiaiLogo from '~/assets/media/svgs/quasiai-logo.vue'
</script>
