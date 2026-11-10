<script setup lang="ts">
import Heading from './components/Heading.vue';
import Hero from './components/Hero.vue';
import Navbar from './components/Navbar.vue';
import SpecialityCard from './components/SpecialityCard.vue';
import Projects from './components/Projects.vue';
import Steps from './components/Steps.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <Navbar />
  <Hero />
  <Heading heading="Curated for Best Outcome" description = "From modern cloud applications to custom machine learning pipelines, we architect technology that meets strict operational demands."/>
  <SpecialityCard />
  <Heading heading="Architecting Systems & Applications" description="Explore selected client and internal systems built with scalable architecture, secure backend services, and modern user experiences." />
  <Projects />
  <Steps />
  <Footer />
</template>
