<template>
  <!-- <v-sheet
    width="100px"
    height="120px"
    rounded
    elevation="8"
    class="pa-4"
  >
    <div style="height: 80%;">
      <v-img
        :src="props.urlRef"
        alt="Skills Icon"
        contain
        height="100%"
        width="100%"
      ></v-img>
    </div>
    <div style="text-align: center; padding-top: 4px; font-weight: bold;">{{ props.skillTitle }} </div>

  </v-sheet> -->

  <v-card class="mx-auto" :subtitle="description" width="300" hover>
    <template v-slot:title>
      <span class="font-weight-black">{{ skillTitle }}</span>
    </template>

    <template v-slot:prepend>
      <v-icon :color="iconColor" :size="'50px'" :icon="icon"></v-icon>
    </template>

  </v-card>
</template>

<script setup lang="ts">
const props = defineProps({
  icon: String,
  skillTitle: String,
  description: String,
  iconColor: String
});
</script>

<style scoped></style>