<script setup lang="ts">
import SkillsItem from '@/components/SkillsItem.vue';
import TitleGraphic from '@/components/TitleGraphic.vue';
</script>

<template>
  <div style="display: flex; justify-content: center; align-items: center; height: inherit; position: relative;">
    <TitleGraphic title="Overview" />

    <v-sheet width="70%" height="60%" rounded color="transparent">
      <v-container>
        <v-row>
          <v-col v-for="n in 6" cols="auto">
            <SkillsItem skill-title="JavaScript" icon="mdi-language-javascript"
              description="stuff, stuff, stuff, stuff, stuff" icon-color="yellow" />
          </v-col>

        </v-row>
      </v-container>


    </v-sheet>
  </div>
</template>
