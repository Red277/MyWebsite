<template>
  <v-sheet
    width="10%"
    height="20%"
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

  </v-sheet>
</template>

<script setup lang="ts">
  const props = defineProps({
    urlRef: String,
    skillTitle: String
  });
</script>

<style scoped>
</style>