`<template v-if="order === 'left'">

  <v-sheet width="70%" height="60%" rounded color="transparent">
    <v-container class="fill-height" v-if="order === 'left'">
      <v-row class="align-center">

        <v-col> <v-img :src="imageRef"></v-img></v-col>

        <v-col cols="4" class="pa-4">
          <v-row style=" font-size: 40px; font-weight: bolder;"> {{ projectTitle }}</v-row>
          <v-row style="padding-top: 30px;"> {{ description }}</v-row>
          <v-row style="padding-top: 20px;">
            <v-chip class="mr-1" density="compact" color="orange" v-for="tag in tags">{{ tag }}</v-chip>
          </v-row>
          <v-row style="padding-top: 30px;">
            <v-btn v-if="githubUrlRef" class="mr-2" :href="githubUrlRef" target="_blank"><v-icon
                class="pr-2">mdi-github</v-icon>Github</v-btn>
            <v-btn v-if="liveAppUrlRef" :href="liveAppUrlRef"><v-icon class="pr-2">mdi-exit-to-app</v-icon>Live
              App</v-btn>
          </v-row>
        </v-col>
      </v-row>
    </v-container>

    <v-container class="fill-height" v-else-if="order === 'right'">
      <v-row class="align-center fill-height">

        <v-col class="pa-16" style="align-items: center;">
          <v-row style=" font-size: 40px; font-weight: bolder;"> {{ projectTitle }}</v-row>
          <v-row style="padding-top: 30px;"> {{ description }}</v-row>
          <v-row style="padding-top: 20px;">
            <v-chip class="mr-1" density="compact" color="orange" v-for="tag in tags">{{ tag }}</v-chip>
          </v-row>
          <v-row style="padding-top: 30px;">
            <v-btn v-if="githubUrlRef" class="mr-2" :href="githubUrlRef" target="_blank"><v-icon
                class="pr-2">mdi-github</v-icon>Github</v-btn>
            <v-btn v-if="liveAppUrlRef" :href="liveAppUrlRef" target="_blank"><v-icon
                class="pr-2">mdi-exit-to-app</v-icon>Live
              App</v-btn>
          </v-row>
        </v-col>

        <v-col> <v-img src="{{ imageRef  }}"></v-img></v-col>

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
  projectTitle: String,
  order: String,
  imageRef: String
});
</script>
