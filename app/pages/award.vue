<template>
  <section class="bg-[#F8EBD6] min-h-screen py-16 px-4">
    <div class="max-w-6xl mx-auto">

      <!-- Header Section -->
      <div class="text-center mb-16">
        <h1 class="text-4xl md:text-5xl font-black text-[#354E20] uppercase tracking-wider">
          Awards
        </h1>

        <div class="flex items-center justify-center my-4">
          <div class="w-12 h-[2px] bg-[#354E20]/40"></div>
          <span class="mx-4 text-[#354E20] font-bold text-xs uppercase tracking-widest">
            Categories
          </span>
          <div class="w-12 h-[2px] bg-[#354E20]/40"></div>
        </div>

        <p class="text-[#354E20]/80 text-sm md:text-base max-w-md mx-auto font-medium">
          Recognizing excellence and celebrating beer crafting achievements.
        </p>
      </div>

      <!-- Cards Grid -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-stretch">

        <!-- Card 1: Grand Award -->
        <div class="bg-[#DFD8C2] rounded-2xl p-8 shadow-[0_10px_30px_rgba(53,78,32,0.05)] border border-[#354E20]/10 flex flex-col items-center text-center transition-all duration-300 hover:shadow-[0_20px_40px_rgba(53,78,32,0.1)] hover:-translate-y-1">
          <div class="mb-5 text-[#354E20]">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-12 h-12">
              <path fill-rule="evenodd" d="M5.166 2.621v.858c-1.035.148-2.059.33-3.071.543a.75.75 0 0 0-.584.859 6.753 6.753 0 0 0 6.138 5.6 6.73 6.73 0 0 0 2.743 1.346A6.707 6.707 0 0 1 9.279 15H8.54c-1.036 0-1.875.84-1.875 1.875V19.5h-.75a2.25 2.25 0 0 0-2.25 2.25c0 .414.336.75.75.75h15a.75.75 0 0 0 .75-.75 2.25 2.25 0 0 0-2.25-2.25h-.75v-2.625c0-1.036-.84-1.875-1.875-1.875h-.739a6.706 6.706 0 0 1-1.112-3.173 6.73 6.73 0 0 0 2.743-1.347 6.753 6.753 0 0 0 6.139-5.6.75.75 0 0 0-.585-.858 47.077 47.077 0 0 0-3.07-.543V2.62a.75.75 0 0 0-.658-.744 49.22 49.22 0 0 0-6.093-.377c-2.063 0-4.096.128-6.093.377a.75.75 0 0 0-.657.744Zm0 2.629c0 1.196.312 2.32.857 3.294A5.266 5.266 0 0 1 3.16 5.337a45.6 45.6 0 0 1 2.006-.343v.256Zm13.5 0v-.256c.674.1 1.343.214 2.006.343a5.265 5.265 0 0 1-2.863 3.207 6.72 6.72 0 0 0 .857-3.294Z" clip-rule="evenodd" />
            </svg>
          </div>

          <h3 class="text-[#354E20] font-black text-xl mb-2 tracking-wide">GRAND AWARD</h3>
          
          <span class="inline-block bg-[#354E20]/10 text-[#354E20] text-xs font-bold px-4 py-1 rounded-full mb-5">
            Official Competition
          </span>

          <p class="text-[#354E20]/80 text-sm leading-relaxed mb-8 flex-grow">
            Judged strictly by a panel of six international experts using standard BJCP score sheets in a rigorous blind tasting format. 
          </p>

          <!-- Medals Footer -->
          <div class="flex items-center gap-6 pt-4 border-t border-[#354E20]/10 w-full justify-center">
            <div class="flex flex-col items-center gap-1.5">
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-5 h-5 text-amber-500">
    <path d="M7 2h4l1 5H8L7 2Zm6 0h4l-1 5h-4l1-5Z"/>
    <circle cx="12" cy="15" r="6"/>
    <path fill="white" d="M12 11.5l1.03 2.09 2.31.34-1.67 1.63.39 2.3L12 16.77l-2.06 1.09.39-2.3-1.67-1.63 2.31-.34L12 11.5z"/>
  </svg>
  <span class="text-[10px] font-bold uppercase tracking-wider text-[#354E20]/60">
    Gold
  </span>
</div>
            <div class="flex flex-col items-center gap-1.5">
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-5 h-5 text-slate-400">
    <path d="M7 2h4l1 5H8L7 2Zm6 0h4l-1 5h-4l1-5Z"/>
    <circle cx="12" cy="15" r="6"/>
    <text x="12" y="18" text-anchor="middle" font-size="7" fill="white" font-weight="bold">2</text>
  </svg>
  <span class="text-[10px] font-bold uppercase tracking-wider text-[#354E20]/60">
    Silver
  </span>
</div>
           <div class="flex flex-col items-center gap-1.5">
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-5 h-5" style="color:#b45309;">
    <path d="M7 2h4l1 5H8L7 2Zm6 0h4l-1 5h-4l1-5Z"/>
    <circle cx="12" cy="15" r="6"/>
    <text x="12" y="18" text-anchor="middle" font-size="7" fill="white" font-weight="bold">3</text>
  </svg>
  <span class="text-[10px] font-bold uppercase tracking-wider text-[#354E20]/60">
    Bronze
  </span>
</div>
          </div>
        </div>

        <!-- Card 2: People's Choice -->
        <div class="bg-[#DFD8C2] rounded-2xl p-8 shadow-[0_10px_30px_rgba(53,78,32,0.05)] border border-[#354E20]/10 flex flex-col items-center text-center transition-all duration-300 hover:shadow-[0_20px_40px_rgba(53,78,32,0.1)] hover:-translate-y-1">
          <div class="mb-5 text-[#354E20]">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-12 h-12">
              <path fill-rule="evenodd" d="M7.5 6a4.5 4.5 0 1 1 9 0 4.5 4.5 0 0 1-9 0ZM3.751 20.105a8.25 8.25 0 0 1 16.498 0 .75.75 0 0 1-.437.695A18.683 18.683 0 0 1 12 22.5c-2.786 0-5.433-.608-7.812-1.7a.75.75 0 0 1-.437-.695Z" clip-rule="evenodd" />
            </svg>
          </div>

          <h3 class="text-[#354E20] font-black text-xl mb-2 tracking-wide">PEOPLE'S CHOICE</h3>
          
          <span class="inline-block bg-[#354E20]/10 text-[#354E20] text-xs font-bold px-4 py-1 rounded-full mb-5">
            Festival Attendees
          </span>

          <p class="text-[#354E20]/80 text-sm leading-relaxed mb-8 flex-grow">
            Voted on entirely by festival attendees. This award reflects public preference, drinkability, and community popularity.
          </p>

          <!-- People's Choice Footer -->
          <div class="flex items-center gap-6 pt-4 border-t border-[#354E20]/10 w-full justify-center">
            <div class="flex flex-col items-center gap-1.5 text-[#354E20]/70">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-5 h-5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M11.48 3.499c.151-.326.621-.326.772 0l2.115 4.57 4.921.411c.358.03.502.474.227.712l-3.663 3.14 1.011 4.832c.074.354-.306.63-.616.442L12 15.261l-4.246 2.404c-.31.188-.69-.088-.616-.442l1.011-4.832-3.663-3.14c-.275-.238-.131-.682.227-.712l4.921-.411 2.115-4.57Z" />
              </svg>
              <span class="text-[10px] font-bold uppercase tracking-wider text-[#354E20]/60">Top Pick</span>
            </div>
            <div class="flex flex-col items-center gap-1.5 text-[#354E20]/70">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-5 h-5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M6.633 10.25c.896 0 1.7.393 2.267 1.02a2.997 2.997 0 0 1 4.2 0 3.012 3.012 0 0 1 2.267-1.02c1.657 0 3 1.343 3 3 0 2.247-4.14 6.27-5.467 7.493a1.147 1.147 0 0 1-1.6 0C9.94 19.52 5.8 15.497 5.8 13.25c0-1.657 1.343-3 3-3Z" />
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 3v3.75m0 0a3.75 3.75 0 1 0 0 7.5 3.75 3.75 0 0 0 0-7.5Z" />
              </svg>
              <span class="text-[10px] font-bold uppercase tracking-wider text-[#354E20]/60">Runner Up</span>
            </div>
            <div class="flex flex-col items-center gap-1.5 text-[#354E20]/70">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-5 h-5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M18 18.72a9.094 9.094 0 0 0 3.741-.479 3 3 0 0 0-4.682-2.72m.94 3.198.001.031c0 .225-.012.447-.037.666A11.944 11.944 0 0 1 12 21c-2.17 0-4.207-.576-5.963-1.584A6.062 6.062 0 0 1 6 18.719m12 0a5.971 5.971 0 0 0-.941-3.197m0 0A5.995 5.995 0 0 0 12 12.75a5.995 5.995 0 0 0-5.058 2.772m0 0a3 3 0 0 0-4.681 2.72 8.986 8.986 0 0 0 3.74.477m.94-3.197a5.971 5.971 0 0 0-.94 3.197M15 6.75a3 3 0 1 1-6 0 3 3 0 0 1 6 0Zm6 3a2.25 2.25 0 1 1-4.5 0 2.25 2.25 0 0 1 4.5 0Zm-13.5 0a2.25 2.25 0 1 1-4.5 0 2.25 2.25 0 0 1 4.5 0Z" />
              </svg>
              <span class="text-[10px] font-bold uppercase tracking-wider text-[#354E20]/60">Third Place</span>
            </div>
          </div>
        </div>

        <!-- Card 3: Excellence Award -->
        <div class="bg-[#DFD8C2] rounded-2xl p-8 shadow-[0_10px_30px_rgba(53,78,32,0.05)] border border-[#354E20]/10 flex flex-col items-center text-center transition-all duration-300 hover:shadow-[0_20px_40px_rgba(53,78,32,0.1)] hover:-translate-y-1">
          <div class="mb-5 text-[#354E20]">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-12 h-12">
              <path fill-rule="evenodd" d="M10.788 3.21c.448-1.077 1.976-1.077 2.424 0l2.082 5.006 5.404.434c1.164.093 1.636 1.545.749 2.305l-4.117 3.527 1.257 5.273c.271 1.136-.964 2.033-1.96 1.425L12 18.354 7.373 21.18c-.996.608-2.231-.29-1.96-1.425l1.257-5.273-4.117-3.527c-.887-.76-.415-2.212.749-2.305l5.404-.434 2.082-5.005Z" clip-rule="evenodd" />
            </svg>
          </div>

          <h3 class="text-[#354E20] font-black text-xl mb-2 tracking-wide">EXCELLENCE AWARD</h3>
          
          <span class="inline-block bg-[#354E20]/10 text-[#354E20] text-xs font-bold px-4 py-1 rounded-full mb-5">
            Innovation & Style
          </span>

          <p class="text-[#354E20]/80 text-sm leading-relaxed mb-8 flex-grow">
            Celebrating technical mastery and boundary-pushing ingredients. Awarded to brewers who show exceptional creativity within their styles.
          </p>

          <!-- Excellence Footer -->
          <div class="flex items-center gap-6 pt-4 border-t border-[#354E20]/10 w-full justify-center">
            <div class="flex flex-col items-center gap-1.5 text-[#354E20]/70">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-5 h-5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M9.813 15.904 9 21l8.982-8.983m-1.963-3.04 1.962-1.962a4.423 4.423 0 0 0-6.255-6.255l-1.962 1.962m0 0 1.962 1.962m-1.962-1.962L3 13.06l1.962 1.962a4.423 4.423 0 0 0 6.255 6.255l1.962-1.962m0 0-1.962-1.963" />
              </svg>
              <span class="text-[10px] font-bold uppercase tracking-wider text-[#354E20]/60">Mastery</span>
            </div>
            <div class="flex flex-col items-center gap-1.5 text-[#354E20]/70">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-5 h-5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 18a3.75 3.75 0 0 0 .495-7.467 5.99 5.99 0 0 0-1.925-3.546 5.974 5.974 0 0 0-2.133-1.257m0 12.27A3.75 3.75 0 0 0 12 18ZM12 18.75h.008v.008H12v-.008ZM9.75 15.75h.008v.008H9.75v-.008ZM14.25 15.75h.008v.008h-.008v-.008Z" />
              </svg>
              <span class="text-[10px] font-bold uppercase tracking-wider text-[#354E20]/60">Innovation</span>
            </div>
            <div class="flex flex-col items-center gap-1.5 text-[#354E20]/70">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-5 h-5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 3v13.5m0-13.5a9 9 0 0 1 9 9c0 2.25-1.5 4.5-4.5 4.5H4.5C1.5 17.25 0 15 0 12.75a9 9 0 0 1 9-9h3Z" />
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 16.5A4.5 4.5 0 0 0 7.5 12h9a4.5 4.5 0 0 0-4.5 4.5Z" />
              </svg>
              <span class="text-[10px] font-bold uppercase tracking-wider text-[#354E20]/60">Style</span>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>