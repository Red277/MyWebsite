<script setup lang="ts">
import ProjectItem from '@/components/ProjectItem.vue';
import TitleGraphic from '@/components/TitleGraphic.vue';

</script>

<template>
  <div style="display: flex; justify-content: center; align-items: center; height: inherit; position: relative;">
    <TitleGraphic title="Projects" />



    <ProjectItem project-title="My Project" description="This is a description of my project."
      :tags="['Vue', 'JavaScript']" github-url-ref="abc.com" live-app-url-ref="abc.com" order="left" />


  </div>
</template>
