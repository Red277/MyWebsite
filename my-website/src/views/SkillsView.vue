<script setup lang="ts">
import SkillsItem from '@/components/SkillsItem.vue';

</script>

<template>
    <div style="display: flex; justify-content: center; align-items: center; height: inherit; position: relative;">
    <p style="text-align: left; font-size:2rem; top: 100px; position: absolute ;">Skills</p>
    
      <v-sheet
        width="60%"
        height="60%"
        rounded
        class="position-"
      >
        <SkillsItem skill-title="JavaScript" url-ref="/src/assets/javascript.svg"/>

      </v-sheet>
    </div>
</template>
