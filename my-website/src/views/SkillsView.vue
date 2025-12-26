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
        <v-container>
          <v-row>
            <v-col
              v-for="n in 10"
              cols="auto"
            >
              <SkillsItem skill-title="JavaScript" url-ref="/src/assets/javascript.svg"/>
            </v-col>

          </v-row>
        </v-container>


      </v-sheet>
    </div>
</template>
