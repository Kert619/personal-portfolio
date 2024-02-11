<template>
  <div class="q-pa-lg">
    <div class="max-width-lg">
      <transition appear enter-active-class="animated zoomIn slower">
        <div class="column items-center">
          <h4 class="text-center text-primary q-mb-sm">About</h4>
          <p class="text-body1 text-center border-b-secondary q-pb-sm">
            A small introduction about me:
          </p>
        </div>
      </transition>

      <transition appear enter-active-class="animated fadeInLeft slower">
        <div class="row justify-center">
          <q-card class="about-card">
            <q-card-section horizontal>
              <q-img class="col-5 gt-xs" src="/about.png" />

              <q-card-section>
                <p class="text-body1">
                  I'm a full-stack web developer proficient in Vue.js, Nuxt.js,
                  and Laravel. I specialize in building dynamic and responsive
                  web applications. With experience in both frontend and backend
                  development, I enjoy creating seamless user experiences and
                  robust functionalities. My skills include designing user
                  interfaces, implementing RESTful APIs, and optimizing database
                  queries. I'm passionate about staying updated with the latest
                  web technologies and constantly improving my coding skills to
                  deliver high-quality solutions.
                </p>
              </q-card-section>
            </q-card-section>

            <q-separator />

            <q-card-actions align="center" class="q-pa-md">
              <q-btn
                icon="download"
                label="Download My Resume"
                color="secondary"
                href="/kert_resume.pdf"
                target="_blank"
              />
            </q-card-actions>
          </q-card>
        </div>
      </transition>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.about-card {
  max-width: 700px;
  width: 100%;
}
</style>
