<template>
  <div class="min-h-screen bg-[#f5eedf]">

    <!-- Header -->
    <div class="max-w-3xl mx-auto px-4 pt-12 pb-8 text-center">
      <p class="text-xs md:text-sm font-semibold tracking-[0.25em] text-gray-500  uppercase mb-3">
        Cambodia Craft Beer Crown 2026
      </p>
      <h1
        class="text-3xl sm:text-4xl md:text-5xl text-[#354D24] font-bold tracking-tight uppercase"
        style="font-family: 'Bebas Neue', sans-serif;">
        Event Schedule
      </h1>
      <div class="flex items-center justify-center gap-4 mt-5">
        <div class="h-px w-20 sm:w-40 bg-[#354D24]  opacity-40"></div>
        <img src="/linelogo.png" alt="Logo" class="w-10 h-10 sm:w-12 sm:h-12 object-contain" />
        <div class="h-px w-20 sm:w-40 bg-[#354D24]  opacity-40"></div>
      </div>
    </div>

    <!-- Timeline -->
    <div class="max-w-2xl mx-auto px-4 sm:px-6 pb-0">
      <div class="relative">

        <!-- Vertical line -->
        <div class="absolute left-7 sm:left-8 top-0 bottom-0 w-px bg-[#354D24]  opacity-20"></div>

        <!-- Opening Ceremony -->
        <div class="relative flex gap-4 sm:gap-6 mb-8 sm:mb-10">
          <div class="w-14 h-14 sm:w-16 sm:h-16 rounded-full border-2 border-[#354D24]  bg-[#f5eedf] flex items-center justify-center shrink-0 z-10 shadow-sm">
            <i class="fa-solid fa-flag text-xl sm:text-2xl text-[#354D24] "></i>
          </div>
          <div class="flex-1 bg-white border border-gray-100 rounded-xl px-4 py-4 sm:px-5 shadow-sm">
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-1">
              <span class="inline-flex items-center gap-1.5 bg-[#354D24] text-white text-xs sm:text-sm font-semibold px-3 py-1 rounded-full w-fit">
                <i class="fa-solid fa-clock text-xs opacity-75"></i>
                02:00 PM
              </span>
             
            </div>
            <h3 class="mt-2.5 text-base sm:text-lg font-bold uppercase tracking-wide text-[#354D24] ">Opening Ceremony</h3>
            <p class="mt-1 text-sm text-gray-500 leading-relaxed">Welcome speech and opening performance to kick off the event.</p>
          </div>
        </div>

        <!-- Activities & Booths -->
        <div class="relative flex gap-4 sm:gap-6 mb-8 sm:mb-10">
          <div class="w-14 h-14 sm:w-16 sm:h-16 rounded-full border-2 border-[#354D24] bg-[#f5eedf] flex items-center justify-center shrink-0 z-10 shadow-sm">
            <i class="fa-solid fa-users text-xl sm:text-2xl text-[#354D24] "></i>
          </div>
          <div class="flex-1 bg-white border border-gray-100 rounded-xl px-4 py-4 sm:px-5 shadow-sm">
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-1">
              <span class="inline-flex items-center gap-1.5 bg-[#354D24]  text-white text-xs sm:text-sm font-semibold px-3 py-1 rounded-full w-fit">
                <i class="fa-solid fa-clock text-xs opacity-75"></i>
                04:00 PM
              </span>

            </div>
            <h3 class="mt-2.5 text-base sm:text-lg font-bold uppercase tracking-wide text-[#354D24] ">Activities & Booths</h3>
            <p class="mt-1 text-sm text-gray-500 leading-relaxed">Explore activities and visit participant booths across the venue.</p>
          </div>
        </div>

        <!-- Dinner Break -->
        <div class="relative flex gap-4 sm:gap-6 mb-8 sm:mb-10">
          <div class="w-14 h-14 sm:w-16 sm:h-16 rounded-full border-2 border-[#354D24]  bg-[#f5eedf] flex items-center justify-center shrink-0 z-10 shadow-sm">
            <i class="fa-solid fa-utensils text-xl sm:text-2xl text-[#354D24] "></i>
          </div>
          <div class="flex-1 bg-white border border-gray-100 rounded-xl px-4 py-4 sm:px-5 shadow-sm">
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-1">
              <span class="inline-flex items-center gap-1.5 bg-[#354D24]  text-white text-xs sm:text-sm font-semibold px-3 py-1 rounded-full w-fit">
                <i class="fa-solid fa-clock text-xs opacity-75"></i>
                07:00 PM
              </span>
            </div>
            <h3 class="mt-2.5 text-base sm:text-lg font-bold uppercase tracking-wide text-[#354D24] ">Dinner Break</h3>
            <p class="mt-1 text-sm text-gray-500 leading-relaxed">Enjoy delicious food, craft beers, and a chance to relax.</p>
          </div>
        </div>

        <!-- Live Performance -->
        <div class="relative flex gap-4 sm:gap-6 mb-8 sm:mb-10">
          <div class="w-14 h-14 sm:w-16 sm:h-16 rounded-full border-2 border-[#354D24]  bg-[#f5eedf] flex items-center justify-center shrink-0 z-10 shadow-sm">
            <i class="fa-solid fa-music text-xl sm:text-2xl text-[#354D24] "></i>
          </div>
          <div class="flex-1 bg-white border border-gray-100 rounded-xl px-4 py-4 sm:px-5 shadow-sm">
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-1">
              <span class="inline-flex items-center gap-1.5 bg-[#354D24]  text-white text-xs sm:text-sm font-semibold px-3 py-1 rounded-full w-fit">
                <i class="fa-solid fa-clock text-xs opacity-75"></i>
                09:00 PM
              </span>
            </div>
            <h3 class="mt-2.5 text-base sm:text-lg font-bold uppercase tracking-wide text-[#354D24] ">Live Performance</h3>
            <p class="mt-1 text-sm text-gray-500 leading-relaxed">Live music and a special show for all attendees.</p>
          </div>
        </div>

        <!-- Closing Ceremony -->
        <div class="relative flex gap-4 sm:gap-6 mb-8 sm:mb-10">
          <div class="w-14 h-14 sm:w-16 sm:h-16 rounded-full border-2 border-[#354D24]  bg-[#f5eedf] flex items-center justify-center shrink-0 z-10 shadow-sm">
            <i class="fa-solid fa-trophy text-xl sm:text-2xl text-[#354D24]  "></i>
          </div>
          <div class="flex-1 bg-white border border-gray-100 rounded-xl px-4 py-4 sm:px-5 shadow-sm">
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-1">
              <span class="inline-flex items-center gap-1.5 bg-[#354D24]  text-white text-xs sm:text-sm font-semibold px-3 py-1 rounded-full w-fit">
                <i class="fa-solid fa-clock text-xs opacity-75"></i>
                11:00 PM
              </span>
            </div>
            <h3 class="mt-2.5 text-base sm:text-lg font-bold uppercase tracking-wide text-[#354D24] ">Closing Ceremony</h3>
            <p class="mt-1 text-sm text-gray-500 leading-relaxed">Awards presentation and closing remarks from the organizers.</p>
          </div>
        </div>

      </div>
    </div>

    <!-- Footer -->
    <footer
      class="relative mt-4 min-h-[140px] h-48 sm:h-64 lg:h-80 bg-bottom bg-no-repeat bg-contain"
      style="background-image: url('/factory.png');"
    >
    </footer>

  </div>
</template>