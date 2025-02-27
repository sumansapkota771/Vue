
<template>
  <Navbar/>
  <HeroSection/>
  <LogoScroll/>
  <PartThree/>
  <!-- <ButtomNavbar/> -->
  </template>

<script>
import HeroSection from './components/HeroSection.vue';
import Navbar from './components/NavbarComponent.vue';
import PartThree from './components/PartThree.vue';
// import ButtomNavbar from './components/BottomNavbar.vue';
// import LogoScroll from './components/LogoScroll.vue';

export default {
  name: 'App',
  components: {
    HeroSection,
    Navbar,
    PartThree,
    // ButtomNavbar,
    // LogoScroll
  }
};

</script>


