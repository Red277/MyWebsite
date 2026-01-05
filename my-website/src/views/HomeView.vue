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
              <v-btn v-bind="props" :color="isHovering ? 'orange' : undefined">VIEW MY WORK</v-btn>
            </RouterLink>
          </v-hover>
        </div>
      </div>

  </div>
</template>

<style>
  .title {
    font-weight: 900;
    font-size: 48px;
    color: rgb(248, 233, 210);
  }

  .highlight{
    font-weight: inherit;
    font-size: inherit;
    color: rgb(218, 141, 0);
  }

</style>