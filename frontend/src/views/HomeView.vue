<script setup lang="ts">
import Navbar from '../components/Navbar.vue'

const categories = [
  { name: 'Construction', icon: '🏗️', count: '24+ Items' },
  { name: 'Power Tools', icon: '🔧', count: '18+ Items' },
  { name: 'Generators', icon: '⚡', count: '12+ Items' },
  { name: 'Landscaping', icon: '🌿', count: '15+ Items' },
]

const featuredEquipment = [
  {
    id: 1,
    name: 'Mini Excavator',
    category: 'Construction',
    price: 120,
    image:
      'https://images.unsplash.com/photo-1504307651254-35680f356dfd?auto=format&fit=crop&w=800&q=80',
  },
  {
    id: 2,
    name: 'Power Generator',
    category: 'Power Equipment',
    price: 45,
    image:
      'https://images.unsplash.com/photo-1581092160607-ee22621dd758?auto=format&fit=crop&w=800&q=80',
  },
  {
    id: 3,
    name: 'Professional Drill',
    category: 'Power Tools',
    price: 25,
    image:
      'https://images.unsplash.com/photo-1504148455328-c376907d081c?auto=format&fit=crop&w=800&q=80',
  },
]
</script>

<template>
  <div class="min-h-screen bg-white text-slate-900">

    <!-- ================= NAVBAR ================= -->
    <Navbar />


    <!-- ================= HERO ================= -->
    <section class="relative overflow-hidden bg-slate-950">

      <!-- Background -->
      <div
        class="absolute inset-0 bg-cover bg-center opacity-30"
        style="
          background-image:
            linear-gradient(to right, rgba(2, 6, 23, 0.9), rgba(2, 6, 23, 0.35)),
            url('https://images.unsplash.com/photo-1504307651254-35680f356dfd?auto=format&fit=crop&w=1800&q=80');
        "
      ></div>

      <div
        class="relative mx-auto flex min-h-[650px] max-w-7xl items-center px-6 py-20 lg:px-8"
      >

        <div class="max-w-3xl">

          <div
            class="mb-6 inline-flex items-center gap-2 rounded-full border border-blue-400/30 bg-blue-500/10 px-4 py-2 text-sm font-medium text-blue-300"
          >
            <span class="h-2 w-2 rounded-full bg-blue-400"></span>
            Reliable equipment. Simple rentals.
          </div>

          <h1
            class="text-4xl font-bold leading-tight text-white sm:text-5xl lg:text-7xl"
          >
            The right equipment
            <span class="text-blue-400">
              for every job.
            </span>
          </h1>

          <p
            class="mt-6 max-w-2xl text-base leading-8 text-slate-300 sm:text-lg"
          >
            Browse quality equipment for construction, maintenance,
            landscaping and more. Rent what you need, when you need it,
            without the hassle.
          </p>


          <!-- Buttons -->
          <div class="mt-9 flex flex-wrap gap-4">

            <RouterLink
              to="/equipment"
              class="rounded-xl bg-blue-600 px-7 py-3.5 font-semibold text-white shadow-lg shadow-blue-600/20 transition hover:bg-blue-500"
            >
              Browse Equipment
              <span class="ml-2">→</span>
            </RouterLink>

            <a
              href="#how-it-works"
              class="rounded-xl border border-slate-600 bg-slate-900/40 px-7 py-3.5 font-semibold text-white backdrop-blur transition hover:border-slate-400 hover:bg-slate-800"
            >
              How It Works
            </a>

          </div>


          <!-- Small stats -->
          <div
            class="mt-12 flex flex-wrap gap-x-10 gap-y-5 border-t border-slate-700/60 pt-8"
          >

            <div>
              <p class="text-2xl font-bold text-white">50+</p>
              <p class="text-sm text-slate-400">Equipment</p>
            </div>

            <div>
              <p class="text-2xl font-bold text-white">100+</p>
              <p class="text-sm text-slate-400">Happy Customers</p>
            </div>

            <div>
              <p class="text-2xl font-bold text-white">24/7</p>
              <p class="text-sm text-slate-400">Online Access</p>
            </div>

          </div>

        </div>

      </div>
    </section>


    <!-- ================= SEARCH ================= -->
    <section class="relative z-10 mx-auto -mt-10 max-w-6xl px-6">

      <div
        class="rounded-2xl border border-gray-100 bg-white p-5 shadow-xl shadow-slate-200/60 md:p-7"
      >

        <p class="mb-4 text-sm font-semibold text-gray-700">
          What equipment are you looking for?
        </p>

        <div class="flex flex-col gap-3 md:flex-row">

          <div class="relative flex-1">

            <span
              class="absolute left-4 top-1/2 -translate-y-1/2 text-gray-400"
            >
              🔍
            </span>

            <input
              type="text"
              placeholder="Search excavators, generators, drills..."
              class="w-full rounded-xl border border-gray-200 bg-gray-50 py-3.5 pl-11 pr-4 outline-none transition focus:border-blue-500 focus:bg-white focus:ring-4 focus:ring-blue-100"
            />

          </div>

          <RouterLink
            to="/equipment"
            class="flex items-center justify-center rounded-xl bg-blue-600 px-8 py-3.5 font-semibold text-white transition hover:bg-blue-700"
          >
            Search Equipment
          </RouterLink>

        </div>

      </div>

    </section>


    <!-- ================= CATEGORIES ================= -->
    <section class="bg-white py-24">

      <div class="mx-auto max-w-7xl px-6 lg:px-8">

        <div class="flex flex-col justify-between gap-4 sm:flex-row sm:items-end">

          <div>

            <p
              class="text-sm font-bold uppercase tracking-[0.2em] text-blue-600"
            >
              Categories
            </p>

            <h2 class="mt-3 text-3xl font-bold tracking-tight text-slate-900">
              Find equipment by category
            </h2>

            <p class="mt-3 max-w-xl text-gray-500">
              Explore our equipment collection and find the right tools
              for your next project.
            </p>

          </div>

          <RouterLink
            to="/equipment"
            class="font-semibold text-blue-600 transition hover:text-blue-700"
          >
            View all equipment →
          </RouterLink>

        </div>


        <div class="mt-10 grid gap-5 sm:grid-cols-2 lg:grid-cols-4">

          <div
            v-for="category in categories"
            :key="category.name"
            class="group cursor-pointer rounded-2xl border border-gray-200 bg-white p-6 transition duration-300 hover:-translate-y-1 hover:border-blue-200 hover:shadow-xl hover:shadow-slate-200/60"
          >

            <div
              class="flex h-14 w-14 items-center justify-center rounded-xl bg-blue-50 text-2xl transition group-hover:bg-blue-600"
            >
              {{ category.icon }}
            </div>

            <h3 class="mt-5 text-lg font-bold text-slate-900">
              {{ category.name }}
            </h3>

            <p class="mt-1 text-sm text-gray-500">
              {{ category.count }}
            </p>

            <p
              class="mt-5 text-sm font-semibold text-blue-600 opacity-0 transition group-hover:opacity-100"
            >
              Browse category →
            </p>

          </div>

        </div>

      </div>

    </section>


    <!-- ================= FEATURED EQUIPMENT ================= -->
    <section class="bg-slate-50 py-24">

      <div class="mx-auto max-w-7xl px-6 lg:px-8">

        <div class="text-center">

          <p
            class="text-sm font-bold uppercase tracking-[0.2em] text-blue-600"
          >
            Featured Equipment
          </p>

          <h2 class="mt-3 text-3xl font-bold text-slate-900">
            Popular rentals
          </h2>

          <p class="mx-auto mt-3 max-w-2xl text-gray-500">
            Some of our most popular equipment, ready for your next project.
          </p>

        </div>


        <div class="mt-12 grid gap-7 md:grid-cols-2 lg:grid-cols-3">

          <div
            v-for="item in featuredEquipment"
            :key="item.id"
            class="group overflow-hidden rounded-2xl border border-gray-200 bg-white transition duration-300 hover:-translate-y-1 hover:shadow-xl"
          >

            <!-- Image -->
            <div class="relative h-60 overflow-hidden bg-gray-200">

              <img
                :src="item.image"
                :alt="item.name"
                class="h-full w-full object-cover transition duration-500 group-hover:scale-105"
              />

              <div
                class="absolute left-4 top-4 rounded-full bg-green-100 px-3 py-1 text-xs font-semibold text-green-700"
              >
                Available
              </div>

            </div>


            <!-- Details -->
            <div class="p-6">

              <p class="text-sm font-medium text-blue-600">
                {{ item.category }}
              </p>

              <h3 class="mt-1 text-xl font-bold text-slate-900">
                {{ item.name }}
              </h3>

              <div class="mt-5 flex items-end justify-between">

                <div>

                  <p class="text-xs text-gray-500">
                    Starting from
                  </p>

                  <p class="text-2xl font-bold text-slate-900">
                    ${{ item.price }}
                    <span class="text-sm font-normal text-gray-500">
                      / day
                    </span>
                  </p>

                </div>

                <RouterLink
                  :to="`/equipment/${item.id}`"
                  class="rounded-lg border border-gray-200 px-4 py-2 text-sm font-semibold text-slate-700 transition hover:border-blue-600 hover:bg-blue-600 hover:text-white"
                >
                  View Details
                </RouterLink>

              </div>

            </div>

          </div>

        </div>


        <div class="mt-10 text-center">

          <RouterLink
            to="/equipment"
            class="inline-flex items-center rounded-xl bg-slate-900 px-6 py-3 font-semibold text-white transition hover:bg-slate-800"
          >
            Explore All Equipment
            <span class="ml-2">→</span>
          </RouterLink>

        </div>

      </div>

    </section>


    <!-- ================= HOW IT WORKS ================= -->
    <section
      id="how-it-works"
      class="bg-white py-24"
    >

      <div class="mx-auto max-w-7xl px-6 lg:px-8">

        <div class="text-center">

          <p
            class="text-sm font-bold uppercase tracking-[0.2em] text-blue-600"
          >
            Simple Process
          </p>

          <h2 class="mt-3 text-3xl font-bold text-slate-900">
            Rent equipment in three easy steps
          </h2>

        </div>


        <div class="mt-14 grid gap-10 md:grid-cols-3">

          <!-- Step 1 -->
          <div class="text-center">

            <div
              class="mx-auto flex h-16 w-16 items-center justify-center rounded-2xl bg-blue-600 text-xl font-bold text-white"
            >
              01
            </div>

            <h3 class="mt-6 text-xl font-bold">
              Find Equipment
            </h3>

            <p class="mx-auto mt-3 max-w-xs leading-7 text-gray-500">
              Browse our equipment collection and choose the equipment
              that matches your requirements.
            </p>

          </div>


          <!-- Step 2 -->
          <div class="text-center">

            <div
              class="mx-auto flex h-16 w-16 items-center justify-center rounded-2xl bg-blue-600 text-xl font-bold text-white"
            >
              02
            </div>

            <h3 class="mt-6 text-xl font-bold">
              Choose Your Dates
            </h3>

            <p class="mx-auto mt-3 max-w-xs leading-7 text-gray-500">
              Select your rental period and check the availability
              of your selected equipment.
            </p>

          </div>


          <!-- Step 3 -->
          <div class="text-center">

            <div
              class="mx-auto flex h-16 w-16 items-center justify-center rounded-2xl bg-blue-600 text-xl font-bold text-white"
            >
              03
            </div>

            <h3 class="mt-6 text-xl font-bold">
              Confirm Your Rental
            </h3>

            <p class="mx-auto mt-3 max-w-xs leading-7 text-gray-500">
              Sign in, confirm your rental and manage everything
              directly from your account.
            </p>

          </div>

        </div>

      </div>

    </section>


    <!-- ================= WHY CHOOSE US ================= -->
    <section class="bg-slate-950 py-24 text-white">

      <div
        class="mx-auto grid max-w-7xl items-center gap-14 px-6 lg:grid-cols-2 lg:px-8"
      >

        <div>

          <p
            class="text-sm font-bold uppercase tracking-[0.2em] text-blue-400"
          >
            Why Choose Us
          </p>

          <h2 class="mt-4 text-4xl font-bold leading-tight">
            Equipment rental made
            <span class="text-blue-400">
              simple.
            </span>
          </h2>

          <p class="mt-5 max-w-xl leading-7 text-slate-400">
            Our platform makes it easier to find equipment, check
            availability, submit rental requests and keep track of
            your rentals.
          </p>

          <RouterLink
            to="/equipment"
            class="mt-8 inline-flex rounded-xl bg-blue-600 px-6 py-3 font-semibold transition hover:bg-blue-500"
          >
            Start Browsing
          </RouterLink>

        </div>


        <div class="grid gap-5 sm:grid-cols-2">

          <div class="rounded-2xl border border-slate-800 bg-slate-900 p-6">
            <div class="text-2xl">✓</div>
            <h3 class="mt-4 font-bold">Quality Equipment</h3>
            <p class="mt-2 text-sm leading-6 text-slate-400">
              Reliable equipment suitable for a wide range of projects.
            </p>
          </div>

          <div class="rounded-2xl border border-slate-800 bg-slate-900 p-6">
            <div class="text-2xl">⚡</div>
            <h3 class="mt-4 font-bold">Fast Booking</h3>
            <p class="mt-2 text-sm leading-6 text-slate-400">
              Quickly check availability and submit your rental request.
            </p>
          </div>

          <div class="rounded-2xl border border-slate-800 bg-slate-900 p-6">
            <div class="text-2xl">📋</div>
            <h3 class="mt-4 font-bold">Easy Management</h3>
            <p class="mt-2 text-sm leading-6 text-slate-400">
              Keep track of active, upcoming and previous rentals.
            </p>
          </div>

          <div class="rounded-2xl border border-slate-800 bg-slate-900 p-6">
            <div class="text-2xl">🛡️</div>
            <h3 class="mt-4 font-bold">Secure Platform</h3>
            <p class="mt-2 text-sm leading-6 text-slate-400">
              Secure account access and protected rental information.
            </p>
          </div>

        </div>

      </div>

    </section>


    <!-- ================= CTA ================= -->
    <section class="bg-blue-600 py-20">

      <div class="mx-auto max-w-4xl px-6 text-center text-white">

        <h2 class="text-3xl font-bold sm:text-4xl">
          Ready to get your project started?
        </h2>

        <p class="mx-auto mt-4 max-w-2xl text-blue-100">
          Browse our equipment collection and find exactly what
          you need for your next project.
        </p>

        <RouterLink
          to="/equipment"
          class="mt-8 inline-flex rounded-xl bg-white px-7 py-3.5 font-bold text-blue-600 transition hover:bg-blue-50"
        >
          Browse Equipment →
        </RouterLink>

      </div>

    </section>


    <!-- ================= FOOTER ================= -->
    <footer class="bg-slate-950 text-slate-400">

      <div
        class="mx-auto grid max-w-7xl gap-10 px-6 py-14 md:grid-cols-4 lg:px-8"
      >

        <div class="md:col-span-2">

          <div class="flex items-center gap-3">

            <div
              class="flex h-10 w-10 items-center justify-center rounded-lg bg-blue-600 font-bold text-white"
            >
              ER
            </div>

            <div>

              <p class="font-bold text-white">
                Equipment Rental
              </p>

              <p class="text-xs">
                Management Platform
              </p>

            </div>

          </div>

          <p class="mt-5 max-w-md text-sm leading-6">
            Making equipment rental simple, reliable and accessible
            for every project.
          </p>

        </div>


        <div>

          <h3 class="font-semibold text-white">
            Quick Links
          </h3>

          <div class="mt-4 flex flex-col gap-3 text-sm">

            <RouterLink to="/" class="hover:text-white">
              Home
            </RouterLink>

            <RouterLink to="/equipment" class="hover:text-white">
              Equipment
            </RouterLink>

            <RouterLink to="/about" class="hover:text-white">
              About
            </RouterLink>

            <RouterLink to="/contact" class="hover:text-white">
              Contact
            </RouterLink>

          </div>

        </div>


        <div>

          <h3 class="font-semibold text-white">
            Account
          </h3>

          <div class="mt-4 flex flex-col gap-3 text-sm">

            <RouterLink to="/login" class="hover:text-white">
              Sign In
            </RouterLink>

            <RouterLink to="/register" class="hover:text-white">
              Create Account
            </RouterLink>

          </div>

        </div>

      </div>


      <div class="border-t border-slate-800">

        <div
          class="mx-auto max-w-7xl px-6 py-6 text-center text-sm lg:px-8"
        >
          © 2026 Equipment Rental Management Platform. All rights reserved.
        </div>

      </div>

    </footer>

  </div>
</template>