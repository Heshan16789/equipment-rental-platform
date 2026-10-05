<script setup lang="ts">
import { useRouter } from 'vue-router'

const router = useRouter()

const goToLogin = () => {
  router.push('/login')
}
</script>

<template>
  <nav class="border-b border-gray-200 bg-white">

    <div
      class="mx-auto flex max-w-7xl items-center justify-between px-6 py-4"
    >

      <div class="flex items-center gap-3">

        <div
          class="flex h-10 w-10 items-center justify-center rounded-lg bg-blue-600 font-bold text-white"
        >
          ER
        </div>

        <div>
          <h1 class="font-bold text-gray-900">
            Equipment Rental
          </h1>

          <p class="text-xs text-gray-500">
            Management Platform
          </p>
        </div>

      </div>

      <div class="flex items-center gap-6">

        <a class="cursor-pointer text-sm font-medium text-gray-600">
          Home
        </a>

        <a class="cursor-pointer text-sm font-medium text-gray-600">
          Equipment
        </a>

        <a class="cursor-pointer text-sm font-medium text-gray-600">
          About
        </a>

        <a class="cursor-pointer text-sm font-medium text-gray-600">
          Contact
        </a>

        <button
          @click="goToLogin"
          class="rounded-lg bg-blue-600 px-4 py-2 text-sm font-semibold text-white hover:bg-blue-700"
        >
          Sign In
        </button>

      </div>

    </div>

  </nav>
</template>