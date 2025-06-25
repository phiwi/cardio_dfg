      
<template>
  <!-- 
    This footer will be added to every slide.
    The z-50 class ensures it renders on top of any custom backgrounds.
  -->
  <footer 
    v-if="$slidev.nav.currentPage > 1"
    class="absolute bottom-4 right-6 text-sm text-gray-400 z-50"
  >
    {{ $slidev.nav.currentPage }}
  </footer>
</template>

    