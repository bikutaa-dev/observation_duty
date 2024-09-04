<template>
  <q-layout view="hHr lpR fFr">
    <q-drawer
      show-if-above
      v-model="rightDrawerOpen"
      side="right"
      behavior="desktop"
      bordered
    >
      <!-- drawer content -->
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from 'vue';
import { useQuasar } from 'quasar';
export default {
  setup() {
    const rightDrawerOpen = ref(false);
    const $q = useQuasar();
    $q.dark.toggle();

    return {
      rightDrawerOpen,
      toggleRightDrawer() {
        rightDrawerOpen.value = !rightDrawerOpen.value;
      },
    };
  },
};
</script>
