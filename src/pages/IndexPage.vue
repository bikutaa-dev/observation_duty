<template>
  <q-tabs class="text-teal">
    <q-tab name="Game" icon="sports_esports" label="Game" />
    <q-tab name="Settings" icon="settings" label="Settings" />
  </q-tabs>
  <q-separator />
  <camera-holder />
</template>

<script setup lang="ts">
import CameraHolder from '/components/CameraHolder.vue';
</script>
