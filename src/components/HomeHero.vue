<template>
  <div class="hero text-white overflow-hidden q-pa-lg">
    <div class="max-width-lg relative-position full-height row items-center">
      <transition appear enter-active-class="animated fadeInLeft slower">
        <div class="col col-md-8" :class="{ 'text-center': $q.screen.lt.md }">
          <h1
            class="q-ma-none text-body1"
            style="font-size: 48px; line-height: 1.4"
          >
            Hi, I'm a Web Developer
          </h1>
          <p class="text-subtitle1 text-grey">
            Experienced web developer with a passion for crafting responsive and
            user-friendly websites, proficient in front-end and back-end
            technologies to deliver seamless digital experiences.
          </p>
          <q-btn
            icon="download"
            label="Download My Resume"
            color="secondary"
            href="/kert_resume.pdf"
            target="_blank"
          />
        </div>
      </transition>

      <transition appear enter-active-class="animated fadeInRight slower">
        <q-avatar size="400px" rounded class="absolute-right gt-sm">
          <q-img src="/kert.png" />
        </q-avatar>
      </transition>
    </div>
  </div>
</template>

<script setup lang="ts">
import { useQuasar } from "quasar";

const $q = useQuasar();
</script>

<style scoped lang="scss">
.hero {
  height: 400px;
  background-color: $primary;
}
</style>
