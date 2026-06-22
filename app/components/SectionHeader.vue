<template>
  <div class="text-center mb-10">
    <h1
      class="text-3xl sm:text-4xl md:text-5xl font-bold tracking-tight text-[#354D24]"
      style="font-family: 'Bebas Neue', sans-serif;"
    >
      <slot />
    </h1>
    <div
        class="flex items-center justify-center gap-4 mt-3 md:mt-5 transition-all duration-700 ease-out delay-300"
   >
        <div class="h-px w-20 sm:w-40 md:w-56 bg-[#354D24] opacity-40"></div>
        <img
          src="/linelogo.png"
          alt="Logo"
          class="w-7 h-6 sm:w-7 sm:h-7 md:w-15 md:h-15 object-contain transition-transform duration-700 ease-[cubic-bezier(0.34,1.56,0.64,1)]"
        />
        <div class="h-px w-20 sm:w-40 md:w-56 bg-[#354D24] opacity-40"></div>
      </div>
  </div>
</template>