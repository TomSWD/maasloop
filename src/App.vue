<template>
  <div>
    <NavSection />
    <HeroSection />
    <InfoSection />
    <CalcSection />
    <CtaSection />
  </div>
</template>

<script>
import "@/assets/styles/reset.css";
import "@/assets/styles/global.css";

import NavSection from "./components/NavSection.vue";
import HeroSection from "./components/HeroSection.vue";
import InfoSection from "./components/InfoSection.vue";
import CalcSection from "./components/CalcSection.vue";
import CtaSection from "./components/CtaSection.vue";

export default {
  name: "App",
  components: {
    NavSection,
    HeroSection,
    InfoSection,
    CalcSection,
    CtaSection,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700;900&display=swap");
</style>
