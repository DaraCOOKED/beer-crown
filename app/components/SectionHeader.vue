<template>
  <div class="text-center mb-10">
    <h1
      class="text-3xl sm:text-4xl md:text-5xl font-bold tracking-tight text-[#354D24]"
      style="font-family: 'Bebas Neue', sans-serif;"
    >
      <slot />
    </h1>
    <div class="flex items-center justify-center gap-4 mt-4">
      <div class="h-px w-20 sm:w-40 bg-green-700 opacity-40"></div>
      <img src="/linelogo.png" alt="Logo" class="w-10 h-10 object-contain" />
      <div class="h-px w-20 sm:w-40 bg-green-700 opacity-40"></div>
    </div>
  </div>
</template>