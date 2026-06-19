<template>
  <div class="min-h-screen flex flex-col bg-[#F7EBD5] text-stone-900">
    <header class="sticky top-0 z-50 bg-[#F7EBD5] text-amber-50">
      <div class="flex items-center justify-between px-4 py-3">
        <NuxtLink to="/" class="text-lg font-bold tracking-wide">
          <img src="/logo-company.png" alt="Beer Crown 2026 logo">
        </NuxtLink>

        <button @click="menuOpen = true" class="md:hidden flex flex-col gap-1" aria-label="Open menu">
          <span class="block w-6 h-1 bg-[#000]"></span>
          <span class="block w-6 h-1 bg-[#000]"></span>
          <span class="block w-6 h-1 bg-[#000]"></span>
        </button>

        <nav class="hidden md:flex gap-6 text-[#036533] text-sm font-medium">
          <NuxtLink
            to="/"
            exact-active-class=" underline underline-offset-4"
            class="hover:text-amber-300 transition-colors"
          >Home</NuxtLink>

          <NuxtLink
            to="/brewerise"
            active-class=" underline underline-offset-4"
            class="hover:text-amber-300 transition-colors"
          >Breweries</NuxtLink>

          <NuxtLink
            to="/schedule"
            active-class=" underline underline-offset-4"
            class="hover:text-amber-300 transition-colors"
          >Schedule</NuxtLink>

          <NuxtLink
            to="/beer-style"
            active-class="text-black underline underline-offset-4"
            class="hover:text-amber-300 transition-colors"
          >Beer styles</NuxtLink>

          <NuxtLink
            to="/award"
            active-class=" underline underline-offset-4"
            class="hover:text-amber-300 transition-colors"
          >Awards</NuxtLink>

          <NuxtLink
            to="/sponsor"
            active-class=" underline underline-offset-4"
            class="hover:text-amber-300 transition-colors"
          >Sponsors</NuxtLink>
        </nav>
      </div>
    </header>

    <!-- Mobile backdrop -->
    <Transition name="fade">
      <div
        v-if="menuOpen"
        class="md:hidden fixed inset-0 z-[60] bg-stone-900/40"
        @click="menuOpen = false"
      ></div>
    </Transition>

    <!-- Mobile sidebar -->
    <Transition name="slide">
      <aside
        v-if="menuOpen"
        class="md:hidden fixed inset-y-0 left-0 z-[70] w-80 max-w-[85%] bg-white shadow-xl overflow-y-auto"
      >
        <!-- Drawer header -->
        <div class="flex items-center justify-between px-2 py-4 border-b border-stone-100">
          <span class="font-semibold text-sm">
            <img src="/logo-company.png" alt="">
          </span>
          <button @click="menuOpen = false" aria-label="Close menu" class="text-amber-500 px-2">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M6 6l12 12M18 6L6 18" stroke-linecap="round"/>
            </svg>
          </button>
        </div>

        <!-- Nav links -->
        <nav class="flex flex-col gap-5 px-5 py-6 text-sm text-[#036533] font-medium">
          <NuxtLink
            to="/"
            exact-active-class="text-amber-600 underline underline-offset-4"
            @click="menuOpen = false"
            class="hover:text-amber-600"
          >Home</NuxtLink>
          <NuxtLink
            to="/award"
            active-class="text-amber-600 underline underline-offset-4"
            @click="menuOpen = false"
            class="hover:text-amber-600"
          >Award</NuxtLink>
          <NuxtLink
            to="/schedule"
            active-class="text-amber-600 underline underline-offset-4"
            @click="menuOpen = false"
            class="hover:text-amber-600"
          >Schedule</NuxtLink>
          <NuxtLink
            to="/sponsor"
            active-class="text-amber-600 underline underline-offset-4"
            @click="menuOpen = false"
            class="hover:text-amber-600"
          >Sponsors</NuxtLink>
          <NuxtLink
            to="/brewerise"
            active-class="text-amber-600 underline underline-offset-4"
            @click="menuOpen = false"
            class="hover:text-amber-600"
          >Breweries</NuxtLink>
          <NuxtLink
            to="/beer-style"
            active-class="text-amber-600 underline underline-offset-4"
            @click="menuOpen = false"
            class="hover:text-amber-600"
          >Beer Style</NuxtLink>
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
          <a href="" aria-label="Facebook" class="w-8 h-8 rounded-full bg-stone-900 text-white flex items-center justify-center text-xs font-bold"><i class="fa-brands fa-facebook"></i></a>
          <a href="" aria-label="Instagram" class="w-8 h-8 rounded-full bg-stone-900 text-white flex items-center justify-center"><i class="fa-brands fa-instagram"></i></a>
          <a href="" aria-label="Telegram" class="w-8 h-8 rounded-full bg-stone-900 text-white flex items-center justify-center"><i class="fa-brands fa-telegram"></i></a>
        </div>

        <!-- Search -->
        <div class="px-5 pb-6">
          <div class="relative">
            <input type="text" placeholder="Search" class="w-full bg-stone-100 rounded-md px-4 py-2 text-sm placeholder-stone-400 focus:outline-none" />
            <svg class="absolute right-3 top-1/2 -translate-y-1/2 w-4 h-4 text-stone-500" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <circle cx="11" cy="11" r="7"/><path d="M21 21l-4.3-4.3" stroke-linecap="round"/>
            </svg>
          </div>
        </div>
      </aside>
    </Transition>

    <main class="flex-1">
      <slot />
    </main>
  </div>
</template>

<script setup>
const menuOpen = ref(false)
</script>

<style scoped>
.slide-enter-active,
.slide-leave-active {
  transition: transform 0.3s ease;
}
.slide-enter-from,
.slide-leave-to {
  transform: translateX(-100%);
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>