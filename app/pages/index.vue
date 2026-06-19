<template>
  <section class="relative bg-[#F8EBD6] overflow-hidden px-6 pt-8 pb-6">

    <img src="/ankor.png" alt="" class="absolute -top-3 -right-2 h-95 w-80 object-contain opacity-50 pointer-events-none select-none"/>


    <div class="relative z-10 max-w-[230px]">
      <h1 class="text-[50px] text-[#354D24]" style="font-family: 'Bebas Neue', sans-serif;">
        Event Crown<br />Festival 2026
      </h1>

      <span class="inline-block mt-3 px-3 py-1 bg-[#2F4A2F] text-[#EFE3C8] text-[11px] font-semibold tracking-wide rounded">
        Celebrate. Connect. Enjoy.
      </span>

      <p class="mt-4 text-sm text-stone-800 leading-relaxed">
        Join us for an amazing festival experience with great participants, exciting activities and memorable moment
      </p>
    </div>

 
    <div class="relative z-10 flex justify-end -mt-40 mb-1">
      <img src="/glass.png" alt="Beer glass" class="w-50 drop-shadow-sm" />
    </div>

    <div class="relative z-10 bg-[#F7EBD5] border border-[#000]/15 rounded-xl px-3 py-1">

      <div class="flex items-center gap-4 py-4 border-b border-[#2F4A2F]/25">
        <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#2F4A2F" stroke-width="1.8">
          <rect x="3" y="5" width="18" height="16" rx="2"/>
          <path d="M8 3v4M16 3v4M3 10h18" stroke-linecap="round"/>
        </svg>
        <div>
          <p class="text-[10px] font-semibold tracking-wide text-stone-600">DATE</p>
          <p class="text-sm font-bold text-stone-900">15 - 17 August 2026</p>
        </div>
      </div>

      <div class="flex items-center gap-4 py-4 border-b border-[#2F4A2F]/25">
        <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#2F4A2F" stroke-width="1.8">
          <circle cx="12" cy="12" r="9"/>
          <path d="M12 7v5l3 2" stroke-linecap="round"/>
        </svg>
        <div>
          <p class="text-[10px] font-semibold tracking-wide text-stone-600">TIME</p>
          <p class="text-sm font-bold text-stone-900">02:00 PM - 11:00 PM</p>
        </div>
      </div>

      <div class="flex items-center gap-4 py-4">
        <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#2F4A2F" stroke-width="1.8">
          <path d="M12 21s7-6.5 7-11.5A7 7 0 0 0 5 9.5C5 14.5 12 21 12 21z"/>
          <circle cx="12" cy="9.5" r="2.5"/>
        </svg>
        <div>
          <p class="text-[10px] font-semibold tracking-wide text-stone-600">LOCATION</p>
          <p class="text-sm font-bold text-stone-900">Angkor Wat, Siem Reap</p>
        </div>
      </div>
      

    </div>
    <NuxtLink to="/judge" class="relative z-10 mt-6 flex items-center justify-center gap-3 bg-[#2F4A2F] text-[#EFE3C8] text-lg tracking-wide rounded-xl py-4"style="font-family: 'Bebas Neue', sans-serif;">
  Judge here
  <svg width="22" class="justify-left flex" height="14" viewBox="0 0 24 14" fill="none" stroke="currentColor" stroke-width="2">
    <path d="M1 7h21M16 1l6 6-6 6" stroke-linecap="round" stroke-linejoin="round"/>
  </svg>
</NuxtLink>
<div class="mt-4 bg-[#F8EBD6]  relative border border-[#2F4A2F]/30 rounded-2xl mt-10 px-4 py-6">
 <h2 class="absolute -top-4 left-1/2 -translate-x-1/2
             bg-[#F8EBD6] px-4 text-2xl font-display
             tracking-wide text-[#2F4A2F]">
    Quick Rules
  </h2>

  <div class="grid grid-cols-3">

    <!-- See -->
    <div class="flex flex-col items-center text-center px-2 border-r border-[#F1E8D4]/50">
      <svg width="38" height="26" viewBox="0 0 40 28" fill="none" stroke="#2F4A2F" stroke-width="1.6">
        <path d="M1 14C7 4 33 4 39 14C33 24 7 24 1 14Z" stroke-linejoin="round"/>
        <circle cx="20" cy="14" r="5"/>
      </svg>
      <p class="mt-3 text-sm font-bold uppercase text-stone-900">1. See</p>
      <p class="mt-1 text-xs font-medium text-stone-700 leading-snug">Explore all<br />participants</p>
    </div>

    <!-- Choose -->
    <div class="flex flex-col items-center text-center px-2 border-r border-[#2F4A2F]/50">
      <svg width="32" height="32" viewBox="0 0 36 36" fill="none" stroke="#2F4A2F" stroke-width="1.6">
        <rect x="6" y="6" width="24" height="27" rx="2" stroke-linejoin="round"/>
        <path d="M13 6V4.5a2 2 0 0 1 2-2h6a2 2 0 0 1 2 2V6" stroke-linecap="round"/>
        <path d="M12 19l3.5 3.5L24 14" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
      <p class="mt-3 text-sm font-bold uppercase text-stone-900">1. Choose</p>
      <p class="mt-1 text-xs font-medium text-stone-700 leading-snug">Pick your<br />favorites</p>
    </div>

    <!-- Vote -->
    <div class="flex flex-col items-center text-center px-2">
      <svg width="38" height="30" viewBox="0 0 40 32" fill="none" stroke="#2F4A2F" stroke-width="1.6">
        <rect x="3" y="16" width="34" height="13" rx="1"/>
        <path d="M3 22h34M14 22v7M26 22v7" stroke-width="1"/>
        <path d="M16 16L29 4" stroke-linecap="round"/>
        <path d="M25 3l6 2-2 6" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
      <p class="mt-3 text-sm font-bold uppercase text-stone-900">1. Vote</p>
      <p class="mt-1 text-xs font-medium text-stone-700 leading-snug">Vote and support<br />the best</p>
    </div>

  </div>
</div>

  </section>
</template>