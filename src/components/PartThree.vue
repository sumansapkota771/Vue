<template>
  <div class="align-center text-center mt-20">
    <div class="bg-white text-indigo-600 px-4 py-1 rounded-full text-sm font-semibold shadow-md inline-block">
      Version 2.0 is here!
    </div>
    <h1 class="text-5xl font-bold  text-black mt-4 ">
      {{ message }}
    </h1>
    <br><div class=" flex justify-center items-center">
    <h1 class="mb-50 w-110 scale-140 ">{{ string }}</h1>
  </div>
    <div class="flex justify-between items-center gap-2 mb-10">
      <div class="absolute left-1/6 transform -translate-x-1/2 translate-y-1/2 z-10">
        <img src="../assets/circle.avif" alt="Productivity Illustration" class=" w-50 h-50" />
      </div>
      <div class="flex justify-center items-center relative transform scale-140">
        <img src="../assets/imagescreen.avif" alt="Productivity Illustration" id="imagesection" class="w-full    " />
      </div>
      <div class="absolute right-1/6 transform translate-x-1/2 -translate-y-3/4 z-10">
        <img src="../assets/diamond.avif" alt="diamond" class="w-50 h-50" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'PartThree',
  data() {
    return {
      message: 'A more effective way to track progress',
      string: 'Effortlessly turn your ideas into a fully functional, responsive, no-code SaaS website in just minutes with the set of free components for Framer. '
    };

  },
};
</script>

<style scoped>
#imagesection{

  width: 50%;
  height: 50%;
}</style>
