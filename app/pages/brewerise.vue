<template>
  <div class="min-h-screen bg-[#F7EBD5] px-4 ">

    <!-- Header: page-load fade-up -->
    <div
      class="transition-all item-center justify-center duration-700 ease-out"
      :class="loaded ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-4'"
    >
     <p
        class="text-xs md:text-sm font-semibold text-center mt-4 justify-center tracking-[0.25em] text-gray-500 uppercase mb-3
               transition-all duration-700 ease-out"
        :class="loaded ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-3'"
      >
        Cambodia Craft Beer Crown 2026
      </p>
     <h1
        class="text-3xl md:text-5xl text-center item-center text-[#354D24] font-bold uppercase
               transition-all duration-700 ease-out delay-150"
        :class="loaded ? 'opacity-100 translate-y-0 blur-0' : 'opacity-0 translate-y-4 blur-sm'"
        style="font-family: 'Bebas Neue', sans-serif;"
      >
        Event Schedule
      </h1>
    </div>
      <div
        class="flex items-center justify-center gap-4 mb-4 mt-4 md:mt-5 transition-all duration-700 ease-out delay-300"
        :class="loaded ? 'opacity-100 scale-100' : 'opacity-0 scale-95'"
      >
        <div class="h-px w-20 sm:w-40 md:w-56 bg-[#354D24] opacity-40"></div>
        <div
          role="img"
          aria-label="Logo"
          class="w-10 h-10 sm:w-7 sm:h-7 md:w-9 md:h-9 bg-[#354E20] transition-transform duration-700 ease-[cubic-bezier(0.34,1.56,0.64,1)]"
          :class="loaded ? 'rotate-0 scale-100' : '-rotate-90 scale-50'"
          style="-webkit-mask-image:url('/linelogo.png'); mask-image:url('/linelogo.png'); -webkit-mask-size:contain; mask-size:contain; -webkit-mask-repeat:no-repeat; mask-repeat:no-repeat; -webkit-mask-position:center; mask-position:center;"
        ></div>
        <div class="h-px w-20 sm:w-40 md:w-56 bg-[#354D24] opacity-40"></div>
      </div>
    

    <!-- Grid section: scoped overflow-hidden ONLY here, so it can never clip
         a sticky/fixed element that might live inside SectionHeader/SiteFooter -->
    <div ref="gridSectionRef" class="relative overflow-hidden py-4">

      <!-- Ambient depth blobs: pure CSS gradients, no image files — can never 404/break -->
      <div
        class="absolute -top-10 -left-16 w-72 h-72 sm:w-96 sm:h-96 rounded-full bg-[#F7EBD5] blur-3xl pointer-events-none will-change-transform"
        :style="{ transform: `translateY(${blobADrift}px)` }"
      ></div>
      <div
        class="absolute top-1/2 -right-20 w-72 h-72 sm:w-[28rem] sm:h-[28rem] rounded-full bg-[#3F5A38]/10 blur-3xl pointer-events-none will-change-transform"
        :style="{ transform: `translateY(${blobBDrift}px)` }"
      ></div>

      <div class="relative z-10 max-w-4xl mx-auto grid grid-cols-1 sm:grid-cols-3 lg:grid-cols-3 gap-4 sm:gap-6">

        <div
          :ref="(el) => setCardRef(el, 0)"
          class="relative transition-all duration-700 ease-out hover:-translate-y-1 hover:scale-[1.02] hover:shadow-xl hover:z-10"
          :class="cardVisible[0] ? 'opacity-100 translate-y-0 blur-none scale-100' : 'opacity-0 translate-y-6 blur-sm scale-95'"
          :style="{ transitionDelay: `${waveDelay(0)}ms` }"
        >
          <ParticipantCard
            name="Sak pub"
            description="Sak Pub Craft Beer & Bites is a local brewpub stands out for its impressive selection, pouring up to 12 taps that feature their own small-batch creations alongside other acclaimed brew by Cambodian craft brewer."
            logo="/sakpub.webp"
            facebook="https://www.facebook.com/SakPubCraftBeerBites"
          />
        </div>

        <div
          :ref="(el) => setCardRef(el, 1)"
          class="relative transition-all duration-700 ease-out hover:-translate-y-1 hover:scale-[1.02] hover:shadow-xl hover:z-10"
          :class="cardVisible[1] ? 'opacity-100 translate-y-0 blur-none scale-100' : 'opacity-0 translate-y-6 blur-sm scale-95'"
          :style="{ transitionDelay: `${waveDelay(1)}ms` }"
        >
          <ParticipantCard
            name="Projekt Brews Co."
            description="Projekt Brew Co. is an independent craft brewery based in Kampot,  dedicated to brewing bold, modern beers with a focus on fresh, hop-forward flavours.  From hazy IPAs to experimental fruited sours."
            logo="/projectbrews.webp"
            facebook="https://www.facebook.com/profile.php?id=100063463360069"
          />
        </div>

        <div
          :ref="(el) => setCardRef(el, 2)"
          class="relative transition-all duration-700 ease-out hover:-translate-y-1 hover:scale-[1.02] hover:shadow-xl hover:z-10"
          :class="cardVisible[2] ? 'opacity-100 translate-y-0 blur-none scale-100' : 'opacity-0 translate-y-6 blur-sm scale-95'"
          :style="{ transitionDelay: `${waveDelay(2)}ms` }"
        >
          <ParticipantCard
            name="Botanico Brewing Company"
            description="Located in the heart of Phnom Penh, Botanico is one of the oldest craft breweries in the country, creating a big range of different beers, often using locally grown ingredients. The moto is: Real Cambodian Craft Beer!"
            logo="/newbotanico2.png"
            logo-class="w-40 h-30 sm:w-50 sm:h-24"
            modal-logo-class="w-56 h-39"
            facebook="https://www.facebook.com/botanicobrewingco"
          />
        </div>

        <div
          :ref="(el) => setCardRef(el, 3)"
          class="relative transition-all duration-700 ease-out hover:-translate-y-1 hover:scale-[1.02] hover:shadow-xl hover:z-10"
          :class="cardVisible[3] ? 'opacity-100 translate-y-0 blur-none scale-100' : 'opacity-0 translate-y-6 blur-sm scale-95'"
          :style="{ transitionDelay: `${waveDelay(3)}ms` }"
        >
          <ParticipantCard
            name="Riel Brewing and Distilling"
            description="Established in 2015 in Phnom Penh, Riel Brewing is an independent microbrewery driven by a custom-built, highly automated brewing system. Utilizing premium local and imported ingredients to produce a dynamic, constantly rotating lineup of craft beers, ranging from dialed-in core IPAs to highly experimental, small-batch sours and stouts."
            logo="/riel.png"
            facebook="https://www.facebook.com/rielbrewing"
          />
        </div>

        <div
          :ref="(el) => setCardRef(el, 4)"
          class="relative transition-all duration-700 ease-out hover:-translate-y-1 hover:scale-[1.02] hover:shadow-xl hover:z-10"
          :class="cardVisible[4] ? 'opacity-100 translate-y-0 blur-none scale-100' : 'opacity-0 translate-y-6 blur-sm scale-95'"
          :style="{ transitionDelay: `${waveDelay(4)}ms` }"
        >
          <ParticipantCard
            name="Fuzzy Logic"
            description="Fuzzy Logic is one of the OGs of craft brewing in South East Asia producing award winning ales and our ever popular John Lemon Hard Lemonade."
            logo="/newfuzzy.png"
            facebook="https://www.facebook.com/FuzzyLogicCambodia"
          />
        </div>

        <div
          :ref="(el) => setCardRef(el, 5)"
          class="relative transition-all duration-700 ease-out hover:-translate-y-1 hover:scale-[1.02] hover:shadow-xl hover:z-10"
          :class="cardVisible[5] ? 'opacity-100 translate-y-0 blur-none scale-100' : 'opacity-0 translate-y-6 blur-sm scale-95'"
          :style="{ transitionDelay: `${waveDelay(5)}ms` }"
        >
          <ParticipantCard
            name="Chug Brew"
            description="Chug Brew is a very small nano brewery based in Phnom Penh with a niche heavy metal themed tap room. Our focus is on producing a variety of small batch delicious modern ales."
            logo="/chuglab.webp"
            facebook="https://www.facebook.com/thechuglab"
          />
        </div>

        <div
          :ref="(el) => setCardRef(el, 6)"
          class="relative transition-all duration-700 ease-out hover:-translate-y-1 hover:scale-[1.02] hover:shadow-xl hover:z-10"
          :class="cardVisible[6] ? 'opacity-100 translate-y-0 blur-none scale-100' : 'opacity-0 translate-y-6 blur-sm scale-95'"
          :style="{ transitionDelay: `${waveDelay(6)}ms` }"
        >
          <ParticipantCard
            name="Brew Khnear"
            description="At Brew Khnear, (loosely translated as ‘Brew Together,’) our focus is on getting that work/life balance right.
                      With solid and creative beers made from the finest ingredients using traditional brewing techniques, we strive not to work too hard, but to make time for ourselves and those who are important to us.
                      What better way to bring us all together than drinking good beer."
            logo="/brewkhnear.webp"
            
          />
        </div>

        <div
          :ref="(el) => setCardRef(el, 7)"
          class="relative transition-all duration-700 ease-out hover:-translate-y-1 hover:scale-[1.02] hover:shadow-xl hover:z-10"
          :class="cardVisible[7] ? 'opacity-100 translate-y-0 blur-none scale-100' : 'opacity-0 translate-y-6 blur-sm scale-95'"
          :style="{ transitionDelay: `${waveDelay(7)}ms` }"
        >
          <ParticipantCard
            name="Funghi Art"
            description="Fungi Art is a fermentation company dedicated to maximizing the value of Cambodian rice through craft beer, sake, spirits, and mycoprotein. We believe fermentation can create exceptional flavors while building a more sustainable future for Cambodian agriculture."
            logo="/newfunghi.jpeg"
            facebook="https://www.facebook.com/profile.php?id=100069892638809"
          />
        </div>

        <div
          :ref="(el) => setCardRef(el, 8)"
          class="relative transition-all duration-700 ease-out hover:-translate-y-1 hover:scale-[1.02] hover:shadow-xl hover:z-10"
          :class="cardVisible[8] ? 'opacity-100 translate-y-0 blur-none scale-100' : 'opacity-0 translate-y-6 blur-sm scale-95'"
          :style="{ transitionDelay: `${waveDelay(8)}ms` }"
        >
          <ParticipantCard
            name="Jaya-Vara Meadery"
            description="Jaya Vara. From meadery to brewery, we bring twice the craftsmanship. Two traditions, one passion."
            logo="/jaya.jpg"
            facebook="https://www.facebook.com/profile.php?id=100080223013722"
          />
        </div>

        <div
          :ref="(el) => setCardRef(el, 9)"
          class="relative transition-all duration-700 ease-out hover:-translate-y-1 hover:scale-[1.02] hover:shadow-xl hover:z-10"
          :class="cardVisible[9] ? 'opacity-100 translate-y-0 blur-none scale-100' : 'opacity-0 translate-y-6 blur-sm scale-95'"
          :style="{ transitionDelay: `${waveDelay(9)}ms` }"
        >
          <ParticipantCard
            name="Krama Craft Brewery"
            description="Krama Craft Brewery, based in Siem Reap, Cambodia, is inspired by centuries of brewing tradition and crafts authentic beers that combine heritage, precision, and the finest ingredients. Every pint is brewed with passion and finished with a distinctive French touch."
            logo="/newkrama.png"
            facebook="https://www.facebook.com/profile.php?id=100095224728868"
          />
        </div>

        <div
          :ref="(el) => setCardRef(el, 10)"
          class="relative transition-all duration-700 ease-out hover:-translate-y-1 hover:scale-[1.02] hover:shadow-xl hover:z-10"
          :class="cardVisible[10] ? 'opacity-100 translate-y-0 blur-none scale-100' : 'opacity-0 translate-y-6 blur-sm scale-95'"
          :style="{ transitionDelay: `${waveDelay(10)}ms` }"
        >
          <ParticipantCard
            name="Himawari Microbrewery"
            description="Himawari Microbrewery is the 1st and only microbrewery launched by it’s 5-star hotel-apartments in Cambodia. Made from the finest malt and hops, the beers crafted here are unique in flavour and of the highest quality"
            logo="/himavari.jpg"
            logo-class="w-40 h-24 sm:w-44 sm:h-24"
            modal-logo-class="w-56 h-36"
            facebook="https://www.facebook.com/HimawariHotelMicrobrewery"
          />
        </div>

        <div
          :ref="(el) => setCardRef(el, 11)"
          class="relative transition-all duration-700 ease-out hover:-translate-y-1 hover:scale-[1.02] hover:shadow-xl hover:z-10"
          :class="cardVisible[11] ? 'opacity-100 translate-y-0 blur-none scale-100' : 'opacity-0 translate-y-6 blur-sm scale-95'"
          :style="{ transitionDelay: `${waveDelay(11)}ms` }"
        >
          <ParticipantCard
            name="Bash Brewing"
            description="Bash Brewing is one of the Kingdom’s original craft breweries, creating some of the finest all-natural craft beer in Cambodia."
            logo="/bash.jpg"
            facebook="https://www.facebook.com/bashbrewingkh"
          />
        </div>

      </div>
    </div>

    <!-- Footer: scroll-triggered fade-up -->
    <div
      ref="footerRef"
      class="transition-all duration-700 ease-out"
      :class="footerVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'"
    >
      <SiteFooter />
    </div>

  </div>
</template>

<script setup>
import { ref, reactive, onMounted, onUnmounted } from 'vue'

// =====================================================================
// One-time reveals: page-load cascade for the header, a diagonal
// "wave" stagger per card (triggered the first time each card scrolls
// into view, then unobserved — never re-triggers), and a fade for the
// footer. All driven by opacity/transform/blur only — never layout
// properties — so nothing here can shift the page or resize a card.
// =====================================================================
const loaded = ref(false)
const footerVisible = ref(false)
const footerRef = ref(null)

const cardVisible = reactive(Array(12).fill(false))
const cardRefs = []

function setCardRef(el, index) {
  if (el) cardRefs[index] = el
}

// Diagonal wave: column + row both add delay, so on a 3-column desktop
// grid it cascades like a ripple; on mobile's 1 column it still reads
// as a gentle top-to-bottom sequence since each card's own reveal is
// independently triggered by its own scroll position anyway.
function waveDelay(index) {
  const col = index % 3
  const row = Math.floor(index / 3)
  return (col + row) * 80
}

// =====================================================================
// Continuous ambient parallax: two soft CSS-gradient blobs drifting at
// different speeds/directions behind the grid. No <img> involved, so
// there is no asset path that can 404 or break. Amplitude is a small
// fixed pixel range (not tied to page height), and they live inside a
// `relative overflow-hidden` wrapper scoped ONLY around the grid — not
// the header or footer — so they can never clip an unrelated element.
// =====================================================================
const gridSectionRef = ref(null)
const blobADrift = ref(0)
const blobBDrift = ref(0)

let rawBlobADrift = 0
let rawBlobBDrift = 0
let rafId = null
let isTicking = false
let prefersReducedMotion = false

function clamp(value, min, max) {
  return Math.min(Math.max(value, min), max)
}

function viewportProgress(el) {
  const rect = el.getBoundingClientRect()
  const total = window.innerHeight + rect.height
  return clamp((window.innerHeight - rect.top) / total, 0, 1)
}

function measure() {
  if (!gridSectionRef.value) return
  const progress = viewportProgress(gridSectionRef.value)
  rawBlobADrift = (progress - 0.5) * 70    // settles within ±35px
  rawBlobBDrift = (progress - 0.5) * -100  // settles within ±50px, opposite direction
}

function onScroll() {
  measure()
  if (!isTicking) {
    isTicking = true
    tick()
  }
}

function tick() {
  const diffA = rawBlobADrift - blobADrift.value
  const diffB = rawBlobBDrift - blobBDrift.value
  blobADrift.value += diffA * 0.12
  blobBDrift.value += diffB * 0.12

  if (Math.abs(diffA) > 0.05 || Math.abs(diffB) > 0.05) {
    rafId = requestAnimationFrame(tick)
  } else {
    blobADrift.value = rawBlobADrift
    blobBDrift.value = rawBlobBDrift
    isTicking = false
  }
}

let observer

onMounted(() => {
  prefersReducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches

  if (prefersReducedMotion) {
    loaded.value = true
    footerVisible.value = true
    cardVisible.forEach((_, i) => (cardVisible[i] = true))
    return
  }

  measure()
  tick() // eases blobs in from 0 instead of popping to position

  window.addEventListener('scroll', onScroll, { passive: true })
  window.addEventListener('resize', measure, { passive: true })

  requestAnimationFrame(() => {
    loaded.value = true
  })

  observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (!entry.isIntersecting) return

        const index = cardRefs.indexOf(entry.target)
        if (index !== -1) {
          cardVisible[index] = true
          observer.unobserve(entry.target)
          return
        }
        if (entry.target === footerRef.value) {
          footerVisible.value = true
          observer.unobserve(entry.target)
        }
      })
    },
    { threshold: 0.12 }
  )

  cardRefs.forEach((el) => el && observer.observe(el))
  if (footerRef.value) observer.observe(footerRef.value)
})

onUnmounted(() => {
  window.removeEventListener('scroll', onScroll)
  window.removeEventListener('resize', measure)
  if (rafId) cancelAnimationFrame(rafId)
  if (observer) observer.disconnect()
})
</script>

<style scoped>
@media (prefers-reduced-motion: reduce) {
  * {
    transition: none !important;
    animation: none !important;
  }
}
</style>
