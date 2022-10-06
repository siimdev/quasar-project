<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar
            color="teal"
            text-color="white"
            icon="fa-solid fa-scale-balanced"
          />
          Weighting app
        </q-toolbar-title>
        <q-input class="q-pa-sm" standout v-model="text" label="Project name" />
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from "vue";

export default {
  name: "MainLayout",
  components: {},
  setup() {
    return {
      text: ref(""),
    };
  },
};
</script>
