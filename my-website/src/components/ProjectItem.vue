<template>
  <v-sheet width="70%" height="60%" rounded>
    <v-container>
      <v-row>
        <v-col> Image</v-col>


        <v-col class="pa-16" style="position:relative; top: 40px;">
          <v-row style=" font-size: 40px; font-weight: bolder;"> {{ projectTitle }}</v-row>
          <v-row style="padding-top: 30px;"> {{ description }}</v-row>
          <v-row style="padding-top: 20px;">
            <v-chip class="mr-1" density="compact" color="orange" v-for="tag in tags">{{ tag }}</v-chip>
          </v-row>
          <v-row style="padding-top: 30px;">
            <v-btn v-if="githubUrlRef" class="mr-2"><v-icon class="pr-2">mdi-github</v-icon>Github</v-btn>
            <v-btn v-if="liveAppUrlRef"><v-icon class="pr-2">mdi-exit-to-app</v-icon>Live App</v-btn>
          </v-row>

        </v-col>


      </v-row>
    </v-container>
  </v-sheet>
</template>

<script setup lang="ts">
const props = defineProps({
  githubUrlRef: String,
  liveAppUrlRef: String,
  description: String,
  tags: Array,
  projectTitle: String
});
</script>
