
<template>
  <div class="min-h-screen flex flex-col bg-[#F7EBD5]  text-stone-900">
    <header class="sticky top-0 z-50 bg-[#F7EBD5] text-amber-50">
      <div class="flex items-center justify-between px-4 py-3">
        <NuxtLink to="/" class="text-lg font-bold tracking-wide">
          <img src="/logo-company.png" alt="Beer Crown 2026 logo">
        </NuxtLink>
        <button @click="menuOpen = true" class="md:hidden flex flex-col gap-1" aria-label="Open menu">
          <span class="block w-6 h-1 bg-[#000] "></span>
          <span class="block w-6 h-1 bg-[#000] "></span>
          <span class="block w-6 h-1 bg-[#000] "></span>
        </button>
        <nav class="hidden md:flex gap-6 text-sm font-medium">
          <NuxtLink to="/" class="hover:text-amber-300">Home</NuxtLink>
          <NuxtLink to="/brewerise" class="hover:text-amber-300">Breweries</NuxtLink>
          <NuxtLink to="/schedule" class="hover:text-amber-300">Schedule</NuxtLink>
          <NuxtLink to="/beer-style" class="hover:text-amber-300">Beer styles</NuxtLink>
          <NuxtLink to="/award" class="hover:text-amber-300">Awards</NuxtLink>
          <NuxtLink to="/sponsor" class="hover:text-amber-300">Sponsors</NuxtLink>
        </nav>
      </div>
    </header>

    <!-- Mobile drawer -->
    <div
      v-if="menuOpen"
      class="md:hidden fixed inset-0 z-[60] bg-stone-900/40 flex justify-center items-start pt-10 px-4"
      @click.self="menuOpen = false"
    >
      <div class="bg-white rounded-2xl w-full max-w-sm overflow-hidden shadow-xl">

        <!-- Drawer header -->
        <div class="flex items-center justify-between px-5 py-4 border-b border-stone-100">
          <button @click="menuOpen = false" aria-label="Toggle menu" class="text-amber-700">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M4 6h16M4 12h16M4 18h16" stroke-linecap="round"/>
            </svg>
          </button>
          <span class="font-semibold text-sm">Beer Crown 2026</span>
          <button @click="menuOpen = false" aria-label="Close menu" class="text-amber-700">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M6 6l12 12M18 6L6 18" stroke-linecap="round"/>
            </svg>
          </button>
        </div>

        <!-- Nav links -->
        <nav class="flex flex-col items-center gap-5 py-6 text-sm font-medium">
          <NuxtLink to="/" @click="menuOpen=false" class="text-amber-600">Home</NuxtLink>
          <NuxtLink to="/award" @click="menuOpen=false" class="hover:text-amber-600">Award</NuxtLink>
          <NuxtLink to="/schedule" @click="menuOpen=false" class="hover:text-amber-600">Schedule</NuxtLink>
          <NuxtLink to="/sponsor" @click="menuOpen=false" class="hover:text-amber-600">Sponsors</NuxtLink>
          <NuxtLink to="/participants" @click="menuOpen=false" class="hover:text-amber-600">Breweries</NuxtLink>
          <NuxtLink to="/beer-style" @click="menuOpen=false" class="hover:text-amber-600">Beer Style</NuxtLink>
        </nav>

        <!-- Vote button -->
        <div class="flex justify-center pb-5">
          <button class="px-8 py-2 rounded-full bg-amber-200 text-stone-800 text-sm font-medium hover:bg-amber-300">
            Vote here
          </button>
        </div>

        <!-- Social -->
        <p class="text-center text-xs text-stone-500 mb-3">Our social</p>
        <div class="flex justify-center gap-3 mb-5">
          <a href="#" aria-label="Facebook" class="w-8 h-8 rounded-full bg-stone-900 text-white flex items-center justify-center text-xs font-bold">f</a>
          <a href="#" aria-label="Pinterest" class="w-8 h-8 rounded-full bg-stone-900 text-white flex items-center justify-center text-xs font-bold">p</a>
          <a href="#" aria-label="Telegram" class="w-8 h-8 rounded-full bg-stone-900 text-white flex items-center justify-center">
            <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M21.5 4.5L2.5 12l6 2 2 6 3-4 5 4 3-19.5z"/></svg>
          </a>
        </div>

        <!-- Search -->
        <div class="px-5 pb-5">
          <div class="relative">
            <input type="text" placeholder="Search" class="w-full bg-stone-100 rounded-md px-4 py-2 text-sm placeholder-stone-400 focus:outline-none" />
            <svg class="absolute right-3 top-1/2 -translate-y-1/2 w-4 h-4 text-stone-500" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <circle cx="11" cy="11" r="7"/><path d="M21 21l-4.3-4.3" stroke-linecap="round"/>
            </svg>
          </div>
        </div>

      </div>
    </div>

    <main class="flex-1">
      <slot />
    </main>
  </div>
</template>

<script setup>
const menuOpen = ref(false)
</script>    