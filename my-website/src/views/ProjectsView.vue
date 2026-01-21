<script setup lang="ts">
import ProjectItem from '@/components/ProjectItem.vue';
import TitleGraphic from '@/components/TitleGraphic.vue';

//Images

import motmImage from '@/assets/motm-ui-new.png';

</script>

<template>
  <div style="display: flex; justify-content: center; align-items: center; height: inherit; position: relative;">
    <TitleGraphic title="Projects" />



    <ProjectItem project-title="My Project" description="This is a description of my project."
      :tags="['Vue', 'JavaScript']" github-url-ref="https://github.com/apps-of-the-millennium/motm"
      live-app-url-ref="https://motm-b0426.web.app/" order="left" :image-ref="motmImage" />


  </div>
</template>
