<template>
  <div class="relative min-h-screen flex items-center bg-gradient-to-b from-[#d3d3f7] to-[#6a5acd] p-10">
    <div class="w-1/2 text-left md:pl-20 text-white">
      <div class="bg-white text-indigo-600 px-4 py-1 rounded-full text-sm font-semibold shadow-md inline-block">
        Version 2.0 is here!
      </div>
      <h1 class="text-8xl font-bold text-black mt-4">
        Pathway to <span><br>productivity</span>
      </h1>
      <p class="text-lg text-gray-700 mt-4">
        Celebrate the joy of accomplishment with an app designed to track your progress, motivate your efforts, and
        celebrate your successes.
      </p>
      <div class="mt-6 flex space-x-4">
        <button class="bg-black text-white px-6 py-2 rounded-lg font-medium hover:bg-gray-800">Get started</button>
        <button class="text-black text-lg font-medium hover:underline">Learn more →</button>
      </div>
    </div>

    <!-- Floating Image 1 (Top) -->
    <div
      class="absolute top-0 left-1/4 transform scale-50 translate-x-20 translate-y-[-10rem]"
      :style="{ transform: 'translateY(' + image1Position + 'px)' }"
    >
      <img src="../assets/1.png" alt="Productivity Illustration" class="w-full object-contain" />
    </div>

    <!-- Middle Image -->
    <div class="flex justify-end transform scale-75 animate-float rotate-185">
      <img src="../assets/herocsection.png" alt="Productivity Illustration" class="w-full object-contain" />
    </div>

    <!-- Floating Image 2 (Bottom Right, Slightly Moved Right) -->
    <div
      class="absolute bottom-0 right-0 transform scale-50 translate-x-20 translate-y-40 z-40 rotate-30"
      :style="{ transform: 'translateY(' + image2Position + 'px)' }"
    >
      <img src="../assets/2.png" alt="Productivity Illustration" class="w-full object-contain" />
    </div>
  </div>
</template>

<script>
export default {
  name: "HeroSection",
  data() {
    return {
      image1Position: -150, // initial position for Image 1
      image2Position: 150, // initial position for Image 2
    };
  },
  mounted() {
    // Listen to scroll events
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeDestroy() {
    // Cleanup the event listener
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      // Get the scroll position
      const scrollY = window.scrollY;

      // Update image positions based on scroll
      this.image1Position = -150 + scrollY * 0.2; // Move image1 upwards as you scroll
      this.image2Position = 150 - scrollY * 0.2; // Move image2 upwards as you scroll
    },
  },
};
</script>

<style scoped>
@keyframes float {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-20px);
  }
  100% {
    transform: translateY(0);
  }
}

.animate-float {
  animation: float 3s ease-in-out infinite;
}
</style>
