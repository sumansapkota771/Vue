<template>
  <nav class="  flex items-center justify-between px-6 py-3 sticky top-0 bg-transparent backdrop-blur-md z-50">
    <!-- Logo -->
    <div class="flex items-center">
      <img src="../assets/logo.svg" alt="Logo" class="w-8 h-8" />
    </div>

    <!-- Navigation Links -->
    <div class="hidden items-center hover:text-black md:flex space-x-6 text-gray-700 pl-4 md:pl-8 lg:pl-12 xl:pl-16">
      <a href="#about" class="hover:text-gray-900">About</a>
      <a href="#features" class="hover:text-gray-900">Features</a>
      <a href="#customers" class="hover:text-gray-900">Customers</a>
      <a href="#updates" class="hover:text-gray-900">Updates</a>
      <a href="#help" class="hover:text-gray-900">Help</a>
      <div>
        <button class="bg-black text-white px-4 py-2 rounded-lg hover:bg-gray-800">
          Get for free
        </button>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavbarComponent",
};
</script>

<style scoped>

</style>
