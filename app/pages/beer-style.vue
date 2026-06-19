<template>
  <section class="bg-[#F5EEDC] min-h-screen">
    <div class="max-w-md mx-auto px-5 py-8">

      <!-- Title -->
      <div class="text-center">
        <h1 class="font-title text-[52px] text-[#3F5A38]">
          BEER STYLE
        </h1>

        <div class="flex justify-center items-center gap-3 mt-2">
          <div class="w-16 h-[2px] bg-[#3F5A38]"></div>
          <span class="text-[#3F5A38]">✦</span>
          <div class="w-16 h-[2px] bg-[#3F5A38]"></div>
        </div>
      </div>

      <!-- Theme -->
<div class="mt-8 relative border border-[#B68C3A] rounded-[40px] py-5 pl-8 pr-28 flex items-center min-h-[90px]">
  
  <div class="relative z-10">
    <h2 class="text-[16px] font-bold text-[#3F5A38] leading-none tracking-tight">
      2026 THEME
    </h2>

    <p class="text-[#3F5A38] text-[15px] font-medium mt-1.5 leading-snug">
      Classic European Beer<br>styles.
    </p>
  </div>

  <div class="absolute -right-4 top-1/2 -translate-y-1/2 pointer-events-none">
    <img
      src="/Barrel1.png"
      alt="Barrel Theme"
      class="w-50 h-auto object-contain drop-shadow-sm"
    >
  </div>
  
</div>

      <!-- About -->
      <div class="mt-6 border border-[#B68C3A] rounded-[30px] p-6">
        <h2 class="font-title text-2xl text-[#3F5A38] mb-4">
          ABOUT THE COMPETITION
        </h2>

        <p class="text-[#3F5A38] leading-relaxed">
          This competition is Part 1 of the annual Beer Crown Trilogy.
          Each year highlights a different brewing tradition and style.
          The 2026 edition celebrates Classic European Beer Styles.
        </p>
      </div>

  <fieldset class="mt-6 border border-[#B68C3A] rounded-[30px] px-6 pb-6 pt-2">
  
  <legend class="ml-6 px-3 text-base  font-bold text-[#3F5A38] tracking-wide bg-[#F5EEDC]">
    ALLOWED STYLE
  </legend>

  <div class="grid grid-cols-2 gap-5 mt-4">
    <div
      v-for="style in styles"
      :key="style"
      class="flex items-center gap-3"
    >
      <div class="w-9 h-9 bg-[#3F5A38] rounded-full flex justify-center items-center flex-shrink-0">
        <svg
          class="w-4 h-4"
          viewBox="0 0 24 24"
          fill="none"
          stroke="white"
          stroke-width="2"
        >
          <path d="M7 4h8v8a4 4 0 0 1-8 0V4z"/>
          <path d="M15 6h2a2 2 0 0 1 2 2v2a3 3 0 0 1-3 3h-1"/>
          <path d="M9 20h4"/>
          <path d="M11 16v4"/>
        </svg>
      </div>

      <span class="text-sm font-medium text-[#3F5A38]">
        {{ style }}
      </span>
    </div>
  </div>

</fieldset>
      <!-- Note -->
      <div class="mt-6 border border-[#B68C3A] rounded-full px-6 py-4">
        <p class="text-sm text-[#3F5A38]">
          <strong>Note:</strong>
          Only beer styles listed above are eligible for the 2026 competition.
        </p>
      </div>

      <!-- Decoration -->
      <div class="mt-8 -mx-5">
        <img
          src="/image-25.png"
          alt="Decoration"
          class="w-full"
        >
      </div>

    </div>
  </section>
</template>

<script setup>
const styles = [
  "Pilsner",
  "Belgian Ale",
  "Lager",
  "Bock",
  "Porter",
  "Wheat Beer",
  "Stout"
]
</script>