<template>
  <q-layout view="hHh lpR fff">
    <q-header
      bordered
      class="bg-primary text-white row justify-center items-center"
    >
      <q-toolbar class="q-pa-sm full-width" style="max-width: 1200px">
        <q-btn
          dense
          flat
          round
          icon="menu"
          class="lt-sm"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg" />
          </q-avatar>
          Title
        </q-toolbar-title>

        <div class="row q-gutter-x-sm gt-xs">
          <q-btn flat label="Home" @click="scrollTo()" />
          <q-btn flat label="Projects" @click="scrollTo('#projects')" />
          <q-btn flat label="Education" @click="scrollTo('#education')" />
          <q-btn flat label="About" @click="scrollTo('#about')" />
        </div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" side="left" behavior="mobile" bordered>
      <!-- drawer content -->
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer bordered class="bg-primary text-white">
      <p class="q-ma-sm text-center text-body1">
        Copyright 2024. All rights reserved.
      </p>
    </q-footer>
  </q-layout>
</template>

<script setup lang="ts">
import { ref } from "vue";

const leftDrawerOpen = ref(false);
const toggleLeftDrawer = () => {
  leftDrawerOpen.value = !leftDrawerOpen.value;
};

const scrollTo = (selector: string | null = null) => {
  if (selector) {
    const content = document.querySelector(selector);
    content?.scrollIntoView({ behavior: "smooth" });
    history.replaceState(null, "", selector);
  } else {
    window.scrollTo({ top: 0, behavior: "smooth" });
    history.replaceState(null, "", "/");
  }
};
</script>
