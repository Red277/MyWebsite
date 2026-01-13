<script setup lang="ts">
import TitleGraphic from '@/components/TitleGraphic.vue';
</script>


<template>
  <div style="display: flex; justify-content: center; align-items: center; height: inherit; position: relative;">
    <TitleGraphic title="About" />
    <v-container>
      <v-row no-gutters align="center">
        <v-col>
          <v-sheet class="pa-4 ma-2">
            It is a long established fact that a reader will be distracted by the readable content of a page when
            looking at its layout.
            The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to
            using 'Content here, content here',
            making it look like readable English. Many desktop publishing packages and web page editors now use Lorem
            Ipsum as their default model text, and a
            search for 'lorem ipsum' will uncover many web sites still in their infancy. Various versions have evolved
            over the years, sometimes by accident,
            sometimes on purpose (injected humour and the like).
          </v-sheet>
        </v-col>
        <v-col>
          <v-sheet class="pa-2 ma-2">
            <v-avatar image="logo.svg" size="50%"></v-avatar>
          </v-sheet>
        </v-col>

        <v-responsive width="100%"></v-responsive>
      </v-row>
    </v-container>
  </div>
</template>
