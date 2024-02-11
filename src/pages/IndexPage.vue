<template>
  <q-layout view="hHh lpR fff">
    <q-header
      class="bg-primary text-white row justify-center items-center q-py-md"
    >
      <q-toolbar class="q-pa-sm full-width max-width-lg">
        <q-btn
          dense
          flat
          round
          icon="menu"
          class="lt-md"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          <q-avatar>
            <q-img src="/icons/favicon-96x96.png" />
          </q-avatar>
          <span class="q-ml-md">Kert Tatoy</span>
        </q-toolbar-title>

        <div class="row q-gutter-x-sm gt-sm">
          <q-btn
            flat
            label="Home"
            @click="scrollTo()"
            :class="{ active: homeActive }"
          />
          <q-btn
            flat
            label="Services"
            @click="scrollTo('#services')"
            :class="{ active: servicesActive }"
          />
          <q-btn
            flat
            label="Projects"
            @click="scrollTo('#projects')"
            :class="{ active: projectsActive }"
          />
          <q-btn
            flat
            label="Education"
            @click="scrollTo('#education')"
            :class="{ active: educationActive }"
          />
          <q-btn
            flat
            label="Experiences"
            @click="scrollTo('#experiences')"
            :class="{ active: experiencesActive }"
          />
          <q-btn
            flat
            label="About"
            @click="scrollTo('#about')"
            :class="{ active: aboutActive }"
          />
        </div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" side="left" behavior="mobile" bordered>
      <div class="q-pa-md row items-center q-gutter-md">
        <q-avatar>
          <q-img src="/icons/favicon-96x96.png" />
        </q-avatar>
        <span class="text-h6">Kert Tatoy</span>
      </div>

      <q-list bordered>
        <q-item clickable v-ripple @click="scrollTo()">
          <q-item-section class="text-center">Home</q-item-section>
        </q-item>

        <q-item clickable v-ripple @click="scrollTo('#services')">
          <q-item-section class="text-center">Services</q-item-section>
        </q-item>

        <q-item clickable v-ripple @click="scrollTo('#projects')">
          <q-item-section class="text-center">Projects</q-item-section>
        </q-item>

        <q-item clickable v-ripple @click="scrollTo('#education')">
          <q-item-section class="text-center">Education</q-item-section>
        </q-item>

        <q-item clickable v-ripple @click="scrollTo('#experiences')">
          <q-item-section class="text-center">Experiences</q-item-section>
        </q-item>

        <q-item clickable v-ripple @click="scrollTo('#about')">
          <q-item-section class="text-center">About</q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <q-page>
        <div>
          <div id="home" ref="homeRef" class="q-mb-lg">
            <home-hero />
          </div>

          <div id="services" ref="servicesRef" class="q-mb-lg">
            <services />
          </div>

          <div id="projects" ref="projectsRef" class="q-mb-lg">
            <projects />
          </div>

          <div id="education" ref="educationRef" class="q-mb-lg">
            <education />
          </div>

          <div id="experiences" ref="experiencesRef">
            <experience />
          </div>

          <div id="about" ref="aboutRef">
            <about />
          </div>
        </div>

        <q-page-scroller
          position="bottom-right"
          :scroll-offset="150"
          :offset="[18, 18]"
        >
          <q-btn fab-mini icon="keyboard_arrow_up" color="primary" />
        </q-page-scroller>
      </q-page>
    </q-page-container>

    <q-footer bordered class="bg-primary text-white q-pa-md">
      <p class="q-ma-sm text-center text-body1">
        Copyright 2024. All rights reserved.
      </p>
    </q-footer>
  </q-layout>
</template>

<script setup lang="ts">
import { onMounted, ref } from "vue";
import HomeHero from "components/HomeHero.vue";
import Services from "components/Services.vue";
import Projects from "components/Projects.vue";
import Education from "components/Education.vue";
import Experience from "components/Experience.vue";
import About from "components/About.vue";

const leftDrawerOpen = ref(false);

// SECTION ELEMENTS
const homeRef = ref<null | HTMLElement>(null);
const servicesRef = ref<null | HTMLElement>(null);
const projectsRef = ref<null | HTMLElement>(null);
const educationRef = ref<null | HTMLElement>(null);
const aboutRef = ref<null | HTMLElement>(null);
const experiencesRef = ref<null | HTMLElement>(null);

// ACTIVE STATE FOR EACH SECTION
const homeActive = ref(false);
const servicesActive = ref(false);
const projectsActive = ref(false);
const educationActive = ref(false);
const aboutActive = ref(false);
const experiencesActive = ref(false);

// OBSERVE EACH SECTION IF THEY ARE IN THE SCREEN
const observer = new IntersectionObserver(
  (entries: IntersectionObserverEntry[]) => {
    entries.forEach((entry: IntersectionObserverEntry) => {
      const id = entry.target.id;
      // IF CERTAIN SECTION IS VISIBLE ON THE SCREEN, REMOVE ALL ACTIVE STATE AND ADD ACTIVE STATE TO THAT SECTION ONLY
      if (entry.isIntersecting) {
        homeActive.value = false;
        servicesActive.value = false;
        projectsActive.value = false;
        educationActive.value = false;
        aboutActive.value = false;
        experiencesActive.value = false;

        if (id === "home") homeActive.value = true;
        if (id === "services") servicesActive.value = true;
        if (id === "projects") projectsActive.value = true;
        if (id === "education") educationActive.value = true;
        if (id === "experiences") experiencesActive.value = true;
        if (id === "about") aboutActive.value = true;

        if (id === "home") {
          history.replaceState(null, "", "/");
        } else {
          history.replaceState(null, "", "#" + id);
        }
      }
    });
  },
  { root: null, rootMargin: "-400px" }
);

// BEGIN OBSERVING THE SECTIONS WHEN PAGE MOUNTS
onMounted(() => {
  if (homeRef.value) observer.observe(homeRef.value);
  if (servicesRef.value) observer.observe(servicesRef.value);
  if (projectsRef.value) observer.observe(projectsRef.value);
  if (educationRef.value) observer.observe(educationRef.value);
  if (experiencesRef.value) observer.observe(experiencesRef.value);
  if (aboutRef.value) observer.observe(aboutRef.value);
});

// SHOW OR HIDE THE SIDE DRAWER
const toggleLeftDrawer = () => {
  leftDrawerOpen.value = !leftDrawerOpen.value;
};

// SCROLL TO CERTAIN SECTION OF THE PAGE AND CHANGE THE URL ACCORDING TO WHICH SECTION
const scrollTo = (selector: string | null = null) => {
  leftDrawerOpen.value = false;

  setTimeout(() => {
    if (selector) {
      const content = document.querySelector(selector);
      content?.scrollIntoView({ behavior: "smooth" });
    } else {
      window.scrollTo({ top: 0, behavior: "smooth" });
    }
  }, 100);
};
</script>

<style scoped lang="scss">
.active {
  background-color: #264d60;
}
</style>
