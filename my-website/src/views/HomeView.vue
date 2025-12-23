<script setup>
const emit = defineEmits(['activate-navbar'])
</script>
<template>
  <div id="home" style="height: 100vh;">
     <v-hover v-slot="{ isHovering, props }">
          <v-btn @click="emit('activate-navbar')" v-bind="props" :color="isHovering ? 'orange' : undefined">Test</v-btn>
      </v-hover>
  </div>
</template>