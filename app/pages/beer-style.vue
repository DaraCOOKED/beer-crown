<template>
  <section class="bg-[#F5EEDC] min-h-screen" ref="sectionRef">
    <div class="w-full max-w-md md:max-w-2xl lg:max-w-4xl mx-auto px-4 sm:px-6 md:px-8 py-8 md:py-12">

      <!-- Title -->
      <div class="text-center">
        <h1 class="font-title text-4xl md:text-[52px] text-[#3F5A38] leading-tight">
          BEER STYLE
        </h1>
        <div class="flex justify-center items-center gap-3 mt-2 md:mt-4">
          <div class="w-12 md:w-16 h-[2px] bg-[#3F5A38]"></div>
          <span class="text-[#3F5A38]">✦</span>
          <div class="w-12 md:w-16 h-[2px] bg-[#3F5A38]"></div>
        </div>
      </div>

      <!-- Theme -->
      <div class="mt-8 relative border border-[#B68C3A] rounded-[30px] md:rounded-[40px] py-5 pl-6 md:pl-8 pr-24 md:pr-28 flex items-center min-h-[90px]">
        <div class="relative z-10">
          <h2 class="text-[15px] md:text-[16px] font-bold text-[#3F5A38] leading-none tracking-tight">
            2026 THEME
          </h2>
          <p class="text-[#3F5A38] text-[14px] md:text-[15px] font-medium mt-1.5 leading-snug">
            Classic European Beer<br class="hidden sm:inline"> styles.
          </p>
        </div>
        <div
          class="absolute -right-2 md:-right-4 top-1/2 pointer-events-none will-change-transform"
          :style="{ transform: `translateY(calc(-50% + ${barrelOffset}px))` }"
        >
          <img src="/Barrel1.png" alt="Barrel Theme" class="w-50 md:w-50 h-auto object-contain drop-shadow-sm">
        </div>
      </div>

      <!-- About -->
      <div class="mt-6 border border-[#B68C3A] rounded-[24px] md:rounded-[30px] p-5 md:p-6">
        <h2 class="font-title text-xl md:text-2xl text-[#3F5A38] mb-3 md:mb-4">
          ABOUT THE COMPETITION
        </h2>
        <p class="text-[#3F5A38] text-sm md:text-base leading-relaxed">
          This competition is Part 1 of the annual Beer Crown Trilogy.
          Each year highlights a different brewing tradition and style.
          The 2026 edition celebrates Classic European Beer Styles.
        </p>
      </div>

      <!-- Allowed Styles -->
      <fieldset class="mt-6 border border-[#B68C3A] rounded-[24px] md:rounded-[30px] px-5 md:px-6 pb-6 pt-2">
        <legend class="ml-4 md:ml-6 px-3 text-sm md:text-base font-bold text-[#3F5A38] tracking-wide bg-[#F5EEDC]">
          ALLOWED STYLE
        </legend>
        <div class="grid grid-cols-2 lg:grid-cols-4 gap-4 md:gap-5 mt-4">
          <div
            v-for="style in styles"
            :key="style.name"
            class="flex items-center gap-3"
          >
            <div class="w-8 md:w-9 h-8 md:h-9 bg-[#3F5A38] rounded-full flex justify-center items-center flex-shrink-0">
              <svg class="w-3.5 md:w-4 h-3.5 md:h-4" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2">
                <path d="M7 4h8v8a4 4 0 0 1-8 0V4z"/>
                <path d="M15 6h2a2 2 0 0 1 2 2v2a3 3 0 0 1-3 3h-1"/>
                <path d="M9 20h4"/>
                <path d="M11 16v4"/>
              </svg>
            </div>
            <span class="text-sm md:text-base font-medium text-[#3F5A38]">
              {{ style.name }}
            </span>
          </div>
        </div>
      </fieldset>

      <!-- Style Details List -->
      <div class="mt-6 flex flex-col gap-3">
        <div
          v-for="style in styles"
          :key="style.name"
          class="bg-white border border-[#3F5A38]/20 rounded-2xl overflow-hidden grid grid-cols-[100px_1fr]"
        >
          <!-- Image -->
          <div class="relative overflow-hidden min-h-[90px]">
            <img
              :src="style.image"
              :alt="style.name"
              class="w-full h-full object-cover"
              @error="(e) => e.target.style.display = 'none'"
            >
            <span class="absolute top-1.5 left-1.5 text-base bg-white/85 rounded-md px-1 py-0.5 leading-none">
              {{ style.flag }}
            </span>
          </div>

          <!-- Info -->
          <div class="p-3 flex flex-col gap-2 justify-center">
            <div class="flex items-start justify-between gap-2">
              <div>
                <p class="text-[13px] font-bold text-[#3F5A38] leading-snug">{{ style.name }}</p>
                <p class="text-[10px] font-semibold text-[#8a7f6a] uppercase tracking-wider mt-0.5">{{ style.origin }}</p>
              </div>
              <div class="flex gap-1.5 flex-shrink-0 flex-wrap justify-end">
                <span class="text-[10px] font-bold px-2 py-0.5 rounded-full bg-[#FAEEDA] text-[#633806]">{{ style.alcohol }}</span>
                <span class="text-[10px] font-bold px-2 py-0.5 rounded-full bg-[#EAF3DE] text-[#27500A]">IBU {{ style.ibu }}</span>
              </div>
            </div>
            <div class="h-px bg-[#3F5A38]/10"></div>

            <!-- Description with clamp -->
            <p
              class="text-[11px] text-[#5a5a4a] leading-relaxed"
              :style="expandedStyles.has(style.name)
                ? { display: 'block' }
                : { display: '-webkit-box', WebkitLineClamp: 2, WebkitBoxOrient: 'vertical', overflow: 'hidden', maxHeight: '2.8em' }"
            >{{ style.description }}</p>

            <!-- Toggle button -->
            <button
              @click="toggleExpand(style.name)"
              class="self-start text-[10px] font-bold text-[#3F5A38] border border-[#3F5A38]/35 rounded-full px-3 py-0.5 leading-none tracking-wide hover:bg-[#3F5A38]/10 transition-colors duration-150"
            >
              {{ expandedStyles.has(style.name) ? 'Show less ↑' : 'Read more ↓' }}
            </button>

            <div class="h-px bg-[#3F5A38]/10"></div>

            <!-- Extra info grid -->
            <div class="grid grid-cols-2 gap-x-3 gap-y-1.5">
              <div>
                <p class="text-[9px] font-bold text-[#B68C3A] uppercase tracking-wider">Flavor notes</p>
                <p class="text-[11px] text-[#3F5A38] font-medium mt-0.5">{{ style.flavors }}</p>
              </div>
              <div>
                <p class="text-[9px] font-bold text-[#B68C3A] uppercase tracking-wider">Food pairing</p>
                <p class="text-[11px] text-[#3F5A38] font-medium mt-0.5">{{ style.pairing }}</p>
              </div>
              <div>
                <p class="text-[9px] font-bold text-[#B68C3A] uppercase tracking-wider">Serve at</p>
                <p class="text-[11px] text-[#3F5A38] font-medium mt-0.5">{{ style.temp }}</p>
              </div>
              <div>
                <p class="text-[9px] font-bold text-[#B68C3A] uppercase tracking-wider">Beer color</p>
                <p class="text-[11px] text-[#3F5A38] font-medium mt-0.5">{{ style.colorLabel }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Note -->
      <div class="mt-6 relative z-10 border border-[#B68C3A] rounded-2xl md:rounded-full px-5 md:px-6 py-4">
        <p class="text-sm text-[#3F5A38]">
          <strong>Note:</strong>
          Only beer styles listed above are eligible for the 2026 competition.
        </p>
      </div>

      <!-- Decoration with parallax -->
      <div
        class="mt-8 -mx-4 md:mx-0 will-change-transform relative z-0"
        :style="{ transform: `translateY(${decoOffset}px)` }"
      >
        <img src="/image-25.png" alt="Decoration" class="w-full h-auto object-cover md:rounded-3xl">
        <p class="text-center font-title text-lg md:text-xl text-[#3F5A38] mt-3 tracking-wide">
          Celebrating Classic European Brewing Heritage
        </p>
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const styles = [
  {
    name: 'Strong Bitter (ESB)',
    origin: 'England',
    flag: '🇬🇧',
    alcohol: '4.6% – 6.2%',
    ibu: '30 - 50',
    image: 'Strong-Bitter.jpeg',
    description: 'An average- to strong-strength English ale featuring a nice balance between leafy, earthy British hops and a solid malt backbone. Expect notes of biscuit, nut, or caramel with a dry, clean finish.',
    flavors: 'Biscuit · Caramel · Earthy',
    pairing: 'Roast beef · Cheddar',
    temp: '10–13 °C',
    colorLabel: 'Deep amber',
  },
  {
    name: 'English IPA',
    origin: 'England',
    flag: '🇬🇧',
    alcohol: '5.0% – 7.5%',
    ibu: '40 - 60',
    image: 'English-IPA.jpg',
    description: 'A hoppy, moderately strong British pale ale that leans into herbal, floral, and spicy wood qualities rather than the bright citrus of its American cousin. The malt profile is often more prominent, presenting toasted, bready, or caramel layers.',
    flavors: 'Herbal · Toast · Floral',
    pairing: 'Fish & chips · Curry',
    temp: '8–12 °C',
    colorLabel: 'Golden amber',
  },
  {
    name: 'Witbier',
    origin: 'Belgium',
    flag: '🇧🇪',
    alcohol: '4.5% – 5.5%',
    ibu: '8 - 20',
    image: '/Witbier.jpeg',
    description: 'A remarkably refreshing, pale wheat ale brewed with coriander and curaçao orange peel. It is intentionally hazy from unmalted wheat and yeast, offering a bright, citrusy, and subtly spicy flavor profile.',
    flavors: 'Citrus · Coriander · Spice',
    pairing: 'Mussels · Salad · Seafood',
    temp: '3–5 °C',
    colorLabel: 'Pale hazy yellow',
  },
  {
    name: 'Saison',
    origin: 'Belgium',
    flag: '🇧🇪',
    alcohol: '3.5% – 9.5%',
    ibu: '20 - 35',
    image: '/Saison.jpg',
    description: 'An artisanal, highly carbonated Belgian farmhouse ale with a distinctive dry, fruity, and peppery character. It balances complex esters and phenols with a prominent hop bitterness and an incredibly crisp finish.',
    flavors: 'Pepper · Fruit · Spice',
    pairing: 'Grilled chicken · Brie',
    temp: '6–8 °C',
    colorLabel: 'Hazy golden',
  },
  {
    name: 'Weissbier',
    origin: 'Germany',
    flag: '🇩🇪',
    alcohol: '4.3% – 5.6%',
    ibu: '8 - 15',
    image: '/Weissbier-1.jpg',
    description: 'A traditional South German wheat beer famous for its cloudy appearance and dramatic yeast-driven aromas of banana and clove. It has low bitterness, high carbonation, and a fluffy, creamy mouthfeel.',
    flavors: 'Banana · Clove · Vanilla',
    pairing: 'Pretzels · Pork · Sausage',
    temp: '5–7 °C',
    colorLabel: 'Pale hazy gold',
  },
  {
    name: 'German Pils',
    origin: 'Germany',
    flag: '🇩🇪',
    alcohol: '4.4% – 5.2%',
    ibu: '22 - 40',
    image: '/German-Pils.jpeg',
    description: 'A crisp, clean, and highly attenuated gold-colored lager that highlights noble German hops like Hallertau or Tettnanger. It features a distinctive, snappy floral aroma and a firm, lingering bitterness.',
    flavors: 'Floral · Crisp · Grassy',
    pairing: 'Schnitzel · Light salads',
    temp: '4–7 °C',
    colorLabel: 'Pale straw gold',
  },
  {
    name: 'Munich Dunkel',
    origin: 'Germany',
    flag: '🇩🇪',
    alcohol: '4.5% – 5.6%',
    ibu: '18 - 28',
    image: '/Munich-Dunkel.jpg',
    description: 'A classic, deeply comforting dark lager from Bavaria that celebrates rich, bready, and toasty Munich malts. It tastes of bread crusts, nuts, or mild chocolate without ever feeling heavy, overly sweet, or roasted like a stout.',
    flavors: 'Bread · Chocolate · Nuts',
    pairing: 'Roast pork · Dark bread',
    temp: '7–9 °C',
    colorLabel: 'Deep dark brown',
  },
]

// --- Expand/collapse state ---
const expandedStyles = ref(new Set())

function toggleExpand(name) {
  const s = new Set(expandedStyles.value)
  s.has(name) ? s.delete(name) : s.add(name)
  expandedStyles.value = s
}

// --- Parallax ---
const barrelOffset = ref(0)
const decoOffset = ref(0)

function onScroll() {
  const scrollY = window.scrollY
  barrelOffset.value = scrollY * 0.08
  decoOffset.value = scrollY * -0.06
}

onMounted(() => window.addEventListener('scroll', onScroll, { passive: true }))
onUnmounted(() => window.removeEventListener('scroll', onScroll))
</script>