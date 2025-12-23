<script setup>
import HomeView from '@/views/HomeView.vue';
import AboutView from '@/views/AboutView.vue';
import SkillsView from '@/views/SkillsView.vue';
import ProjectsView from '@/views/ProjectsView.vue';
import ContactView from '@/views/ContactView.vue';
import HelloWorld from '@/components/HelloWorld.vue';

const emit = defineEmits(['activate-navbar'])
</script>

<template>
  <div id="home" style="height: 100vh;">
    <HomeView @activate-navbar="$emit('activate-navbar')" />
  </div>
  
  <div id="about" style="height: 100vh; background: gray;">
    <AboutView />
  </div>

  <div id="skills" style="height: 100vh;">
    <SkillsView />
  </div>

  <div id="projects" style="height: 100vh; background: gray;">
    <ProjectsView />
  </div>

    <div id="contact" style="height: 100vh;">
    <ContactView />
  </div>
</template>