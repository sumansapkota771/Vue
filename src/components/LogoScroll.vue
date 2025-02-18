<template>
  <div class="scroller-container overflow-hidden relative">
    <div class="absolute top-0 left-0 w-1/6 h-full z-10 bg-gradient-to-r from-white via-white/70 to-transparent"></div>


    <div class="scroller flex whitespace-nowrap">
      <div v-for="(logo, index) in duplicatedLogos" :key="index" class="logo-item mx-4 flex-shrink-0">
        <img :src="logo" alt="Logo" class="h-12" />
      </div>
    </div>

    <div class="absolute top-0 right-0 w-1/6 h-full z-10 bg-gradient-to-l from-white via-white/70 to-transparent"></div>
  </div>
</template>

<script>
export default {
  name: 'LogoScroller',
  data() {
    return {
      logos: [
        '../assets/Logos/pulse.png',
        '../assets/Logos/pulse1.png',
        '../assets/Logos/pulse1.png',
        '../assets/Logos/pulse1.png',
        '../assets/Logos/pulse1.png',
        '../assets/Logos/pulse1.png'
      ]
    };
  },
  computed: {
    duplicatedLogos() {
      return [...this.logos, ...this.logos]; // Duplicate logos for seamless scrolling
    }
  }
};
</script>

<style scoped>
@keyframes scroll {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-50%);
  }
}

.scroller-container {
  width: 100%;
  display: flex;
  align-items: center;
  overflow: hidden;
  background: white;
  padding: 10px 0;
  position: relative;
}

.scroller {
  display: flex;
  animation: scroll 20s linear infinite;
}
</style>
