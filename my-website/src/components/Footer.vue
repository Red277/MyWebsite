<template>
  <v-footer class="text-center d-flex flex-column ga-2 py-4" color="gray" height="200">
    <div class="d-flex ga-2 pt-6">
      <v-btn
        v-for="icon in icons"
        :key="icon"
        :icon="icon"
        density="comfortable"
        variant="text"
        size="x-large"
      ></v-btn>
    </div>

    <!-- <v-divider class="my-2" thickness="2" width="50"></v-divider> -->


    <v-divider></v-divider>

    <div>
      {{ new Date().getFullYear() }} — <strong>William Li</strong>
    </div>  </v-footer>
</template>

<script setup>
  const icons = [
    'mdi-github',
    'mdi-email',
    'mdi-linkedin'
  ]
</script>