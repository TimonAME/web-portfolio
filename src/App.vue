<template>
  <div class="bg-custom-white overflow-x-hidden bg-[linear-gradient(to_right,rgba(184,184,184,0.1)1px,transparent_1px),linear-gradient(to_bottom,rgba(184,184,184,0.1)1px,transparent_1px)] bg-[size:40px_40px]">
    <!-- Hero Section with Physics Simulation -->
    <PhysicsHero />

    <!-- Compact Horizontal Navigation -->
    <Navigation />

    <!-- Fixed Social Links -->
    <SocialLinks />

    <!-- Content Sections -->
    <div class="container mx-auto">
      <!-- About Me Section -->
      <AboutSection id="about" />

      <!-- Programming Section -->
      <ProgrammingSkillsSection id="skills" />
      <ProgrammingAchievementsSection id="achievements" />
      <ProjectsSection id="projects" />


      <!-- Creative Section -->
      <PhotoSkillsSection id="photography" />
      <PhotoExperienceSection id="experience" />
      <PhotoGallerySection id="photography" />


      <!-- Footer -->
      <FooterSection />
    </div>
  </div>
</template>

<script setup>
import PhysicsHero from './components/PhysicsHero.vue';
import Navigation from './components/Navigation.vue';
import SocialLinks from './components/SocialLinks.vue';
import AboutSection from './components/AboutSection.vue';
import ProjectsSection from './components/ProjectsSection.vue';
import PhotoGallerySection from './components/PhotoGallerySection.vue';
import FooterSection from './components/FooterSection.vue';
import ProgrammingSkillsSection from "@/components/ProgrammingSkillsSection.vue";
import ProgrammingAchievementsSection from "@/components/ProgrammingAchievementsSection.vue";
import PhotoSkillsSection from "@/components/PhotoSkillsSection.vue";
import PhotoExperienceSection from "@/components/PhotoExperienceSection.vue";
</script>

<style>
/* Text Selection Styling */
::selection {
  background-color: #F2921D;
  color: white;
}

/* Scrollbar Styling */
::-webkit-scrollbar {
  width: 12px;
}

::-webkit-scrollbar-track {
  background-color: #f4f4f4;
}

::-webkit-scrollbar-thumb {
  background-color: #2E3440;
  border-radius: 8px;
  border: 3px solid #f4f4f4;
}

* {
  scrollbar-width: thin;
  scrollbar-color: #2E3440 #f4f4f4;
}
</style>