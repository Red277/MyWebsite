<template>
  <div style=" text-align: left; top: 95px; position: absolute;">
    <v-sheet class="rectangle-title" color="orange"></v-sheet>

    <p class=title>
      <span class="greater-than">></span>
      {{ props.title }}
    </p>
  </div>

</template>

<script setup lang="ts">
const icons = [
  'mdi-greater-than',
  'mdi-email',
  'mdi-linkedin'
]

const props = defineProps({
  title: String,
});
</script>

<style>
.title {
  font-weight: 900;
  font-size: 50px;
  color: rgb(241, 241, 241);
  z-index: 2;
  position: relative;
}

.greater-than {
  text-shadow: 0px 1px, 1px 0px, 1px 1px;
  font-weight: 900;
  font-size: 60px;
  color: rgb(218, 141, 0);
  z-index: 2;
  top: -20%;
  left: -40px;
  position: absolute;
}

.rectangle-title {
  top: 68%;
  left: -5px;
  z-index: 1;
  position: absolute;
  width: 80px;
  height: 13%;
}
</style>