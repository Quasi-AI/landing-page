<template>
  <NuxtLayout name="auth-wrapper">
    <div
      class="w-full max-w-[569px] rounded-2xl bg-white py-6 text-center text-2xl lg:shadow-md"
    >
      <NuxtLink to="/">
        <QuasiLogo class="mx-auto w-24 sm:w-28" />
      </NuxtLink>

      <div class="mx-8 flex flex-col gap-4 py-6 sm:mx-12">
        <h1 class="text-left text-lg font-bold">Sign up with email</h1>
        <UInput
          v-model="email"
          type="email"
          placeholder="Enter email"
          maxLength="250"
          size="xl"
          class="w-full"
        />

        <div class="relative">
          <UInput
            :type="isPasswordVisible ? 'text' : 'password'"
            placeholder="Password"
            v-model="password"
            maxLength="250"
            size="xl"
          />
          <span
            class="absolute inset-y-0 right-0 flex cursor-pointer items-center pr-3"
            @click="togglePasswordVisibility"
          >
            <UIcon
              :name="
                isPasswordVisible ? 'i-heroicons-eye' : 'i-heroicons-eye-slash'
              "
            ></UIcon>
          </span>
        </div>

        <UButton
          class="flex w-full justify-center font-bold"
          color="cyan"
          label="Sign up"
          variant="solid"
          size="md"
          :disabled="!isValidEmail(email)"
          @click="signup"
        />
      </div>
      <p class="text-sm">
        Already have an account?
        <NuxtLink to="/auth/login" class="text-[#518aa7]">Sign in</NuxtLink>
      </p>
    </div>
  </NuxtLayout>
</template>

<script setup lang="ts">
import QuasiLogo from '@/assets/media/svgs/quasiai-logo.vue'
import { isValidEmail } from '@/utils/isValidEmail'

const email = ref('')
const password = ref('')
const isPasswordVisible = ref(false)

const signup = () => {
  console.log('signup with:', email.value)
}

const togglePasswordVisibility = () => {
  isPasswordVisible.value = !isPasswordVisible.value
}
</script>
