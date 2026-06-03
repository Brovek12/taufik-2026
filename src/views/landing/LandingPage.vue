<script setup>
import Navbar from '../../components/layouts/Navbar.vue'
import Footer from '../../components/layouts/Footer.vue'

import HeroSection from './sections/HeroSection.vue'
import FeatureSection from './sections/FeatureSection.vue'
import AboutSection from './sections/AboutSection.vue'

import { useScrollReveal } from '../../composables/useScrollReveal'

useScrollReveal()
</script>

<template>
  <Navbar />

  <div class="reveal">
    <HeroSection />
  </div>

  <div class="reveal">
    <FeatureSection />
  </div>

  <div class="reveal">
    <AboutSection />
  </div>

  <Footer />
</template>