<template>
  <NuxtLayout name="auth-wrapper">
    <div
      class="w-full max-w-[569px] rounded-2xl bg-white py-6 text-center text-2xl lg:shadow-md"
    >
      <QuasiLogo class="mx-auto w-24 sm:w-28" />

      <div class="mx-8 flex items-center justify-center gap-4 py-4">
        <GoogleLogo class="cursor-pointer" />
        <FacebookLogo class="cursor-pointer" />
      </div>

      <div class="flex flex-row items-center justify-center gap-4">
        <OrSeperator class="w-3/4 sm:w-2/3" />
      </div>

      <div class="mx-8 flex flex-col gap-4 py-6 sm:mx-12">
        <UText class="text-left text-sm font-bold">Enter your email</UText>
        <UInput
          v-model="email"
          type="email"
          placeholder="Enter email"
          maxLength="250"
          size="xl"
          class="w-full"
        />

        <UButton
          class="flex w-full justify-center font-bold"
          color="cyan"
          label="Continue"
          variant="solid"
          size="md"
          :disabled="!isValidEmail(email)"
          @click="login"
        />
      </div>
    </div>
  </NuxtLayout>
</template>

<script setup lang="ts">
import QuasiLogo from '@/assets/media/svgs/quasiai-logo.vue'
import OrSeperator from '@/assets/media/svgs/or-seperator.vue'
import GoogleLogo from '@/assets/media/svgs/signin-google.vue'
import FacebookLogo from '@/assets/media/svgs/signin-facebook.vue'

const email = ref('')

const isValidEmail = (email: string) => {
  const emailRegex = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$/
  return emailRegex.test(email)
}

const login = () => {
  console.log('Login with:', email.value)
}
</script>
