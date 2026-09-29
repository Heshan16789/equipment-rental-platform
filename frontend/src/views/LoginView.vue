```vue
<script setup lang="ts">
import { ref } from 'vue'

const email = ref('')
const password = ref('')
const rememberMe = ref(false)
const showPassword = ref(false)
const errorMessage = ref('')

const handleLogin = () => {
  errorMessage.value = ''

  if (!email.value || !password.value) {
    errorMessage.value = 'Please enter your email and password.'
    return
  }

  console.log('Login attempt:', {
    email: email.value,
    rememberMe: rememberMe.value,
  })

  alert('Login functionality will be connected to the backend soon.')
}
</script>

<template>
  <div class="min-h-screen bg-gray-100 flex items-center justify-center px-4 py-8">

    <div class="w-full max-w-5xl bg-white rounded-2xl shadow-xl overflow-hidden md:flex">

      <!-- Left side -->
      <div class="hidden md:flex md:w-1/2 bg-slate-900 text-white p-12 flex-col justify-between">

        <div>
          <div class="flex items-center gap-3 mb-10">
            <div class="w-11 h-11 bg-blue-600 rounded-xl flex items-center justify-center text-xl font-bold">
              ER
            </div>

            <div>
              <h1 class="text-xl font-bold">
                Equipment Rental
              </h1>

              <p class="text-sm text-slate-400">
                Management Platform
              </p>
            </div>
          </div>

          <h2 class="text-4xl font-bold leading-tight mb-6">
            Manage your equipment.
            <span class="text-blue-400">
              Simplify your rentals.
            </span>
          </h2>

          <p class="text-slate-300 leading-relaxed">
            Manage equipment, customers, reservations and rentals
            from one centralized platform.
          </p>
        </div>

        <div class="text-sm text-slate-400">
          © 2026 Equipment Rental Management Platform
        </div>

      </div>


      <!-- Right side -->
      <div class="w-full md:w-1/2 p-8 sm:p-12">

        <!-- Mobile branding -->
        <div class="md:hidden flex items-center gap-3 mb-8">

          <div class="w-11 h-11 bg-blue-600 text-white rounded-xl flex items-center justify-center font-bold">
            ER
          </div>

          <div>
            <h1 class="font-bold text-gray-900">
              Equipment Rental
            </h1>

            <p class="text-sm text-gray-500">
              Management Platform
            </p>
          </div>

        </div>


        <!-- Login heading -->
        <div class="mb-8">

          <h2 class="text-3xl font-bold text-gray-900">
            Welcome back
          </h2>

          <p class="mt-2 text-gray-500">
            Sign in to access your account
          </p>

        </div>


        <!-- Error message -->
        <div
          v-if="errorMessage"
          class="mb-5 rounded-lg bg-red-50 border border-red-200 px-4 py-3 text-sm text-red-700"
        >
          {{ errorMessage }}
        </div>


        <!-- Login form -->
        <form @submit.prevent="handleLogin" class="space-y-5">

          <!-- Email -->
          <div>

            <label
              for="email"
              class="block text-sm font-medium text-gray-700 mb-2"
            >
              Email address
            </label>

            <input
              id="email"
              v-model="email"
              type="email"
              placeholder="you@example.com"
              class="w-full rounded-lg border border-gray-300 px-4 py-3 outline-none transition focus:border-blue-500 focus:ring-2 focus:ring-blue-100"
            />

          </div>


          <!-- Password -->
          <div>

            <div class="flex items-center justify-between mb-2">

              <label
                for="password"
                class="block text-sm font-medium text-gray-700"
              >
                Password
              </label>

              <button
                type="button"
                class="text-sm font-medium text-blue-600 hover:text-blue-700"
              >
                Forgot password?
              </button>

            </div>

            <div class="relative">

              <input
                id="password"
                v-model="password"
                :type="showPassword ? 'text' : 'password'"
                placeholder="Enter your password"
                class="w-full rounded-lg border border-gray-300 px-4 py-3 pr-20 outline-none transition focus:border-blue-500 focus:ring-2 focus:ring-blue-100"
              />

              <button
                type="button"
                @click="showPassword = !showPassword"
                class="absolute right-3 top-1/2 -translate-y-1/2 text-sm font-medium text-gray-500 hover:text-gray-700"
              >
                {{ showPassword ? 'Hide' : 'Show' }}
              </button>

            </div>

          </div>


          <!-- Remember me -->
          <div class="flex items-center">

            <input
              id="remember"
              v-model="rememberMe"
              type="checkbox"
              class="h-4 w-4 rounded border-gray-300 text-blue-600 focus:ring-blue-500"
            />

            <label
              for="remember"
              class="ml-2 text-sm text-gray-600"
            >
              Remember me
            </label>

          </div>


          <!-- Login button -->
          <button
            type="submit"
            class="w-full rounded-lg bg-blue-600 px-4 py-3 font-semibold text-white transition hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2"
          >
            Sign in
          </button>

        </form>


        <!-- Register -->
        <p class="mt-8 text-center text-sm text-gray-600">

          Don't have an account?

          <button
            type="button"
            class="font-semibold text-blue-600 hover:text-blue-700"
          >
            Create an account
          </button>

        </p>

      </div>

    </div>

  </div>
</template>
```
