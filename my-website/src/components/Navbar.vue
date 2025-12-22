<script>
import { RouterLink } from 'vue-router'
</script>
<template>
  <v-app-bar :elevation="2" color="darken-4" style="opacity: 0.5;">



    <!-- Use RouterLink and set active state to "" to prevent permanent highlighting of Vuetify buttons when using "to" prop with v-btn -->
    <template v-slot:append>
      <v-hover v-slot="{ isHovering, props }">
        <RouterLink to="/#home" active-class="">
          <v-btn v-bind="props" :color="isHovering ? 'orange' : undefined">Home</v-btn>
        </RouterLink>
      </v-hover>

      <v-hover v-slot="{ isHovering, props }">
        <RouterLink to="/#about" active-class="">
          <v-btn v-bind="props" :color="isHovering ? 'orange' : undefined">About</v-btn>
        </RouterLink>
      </v-hover>

      <v-hover v-slot="{ isHovering, props }">
        <RouterLink to="/#skills" active-class="">
          <v-btn v-bind="props" :color="isHovering ? 'orange' : undefined">Skills</v-btn>
        </RouterLink>
      </v-hover>

      <v-hover v-slot="{ isHovering, props }">
        <RouterLink to="/#projects" active-class="">
          <v-btn v-bind="props" :color="isHovering ? 'orange' : undefined">Projects</v-btn>
        </RouterLink>
      </v-hover>

      <v-hover v-slot="{ isHovering, props }">
        <RouterLink to="/#contact" active-class="">
          <v-btn v-bind="props" :color="isHovering ? 'orange' : undefined">Contact</v-btn>
        </RouterLink>
      </v-hover>
    </template>
  </v-app-bar>
</template>

<style scoped>
  .v-app-bar :deep(.v-btn) {
    color: white;
    /* Add other button styles here (e.g., font-weight, text-transform, etc.) */
  }
</style>


