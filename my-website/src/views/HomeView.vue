<script setup lang="ts">
import { RouterLink } from 'vue-router'

</script>
<template>



  <div id="home" style="height: 100vh;">
    <div style="justify-content: center; align-items: center; display: flex; flex-direction: column; height: 90%;">


      <p class="title">Hi, I’m<span class="highlight"> William</span></p> <br>
      <p class="title">a <span class="highlight"> Full Stack Developer</span></p>



      <div style="position: relative; top: 20px;">
        <v-hover v-slot="{ isHovering, props }">
          <RouterLink to="/#about" active-class="">
            <v-btn :size="'large'" v-bind="props" :color="isHovering ? 'orange' : undefined">
              VIEW MY WORK
            </v-btn>
          </RouterLink>
        </v-hover>
      </div>

      <v-icon :size="'50px'" position="absolute" style="top: 20px; color: gray;">
        mdi-chevron-double-down
      </v-icon>
    </div>

  </div>
</template>

<style></style>