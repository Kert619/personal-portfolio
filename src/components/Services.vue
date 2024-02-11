<template>
  <div class="q-pa-lg">
    <div class="max-width-lg">
      <transition appear enter-active-class="animated zoomIn slower">
        <div class="column items-center q-mb-xl">
          <h4 class="text-center text-primary q-mb-sm">
            What Services I'm Providing
          </h4>
          <p class="text-body1 text-center border-b-secondary q-pb-sm">
            Here are some of my expertise:
          </p>
        </div>
      </transition>

      <transition appear enter-active-class="animated slideInUp slower">
        <div class="row justify-center q-gutter-md">
          <q-card class="service-card" flat bordered>
            <div class="q-pa-md">
              <q-img src="/html.png" />
            </div>
            <div
              class="text-caption text-center q-pa-sm bg-primary text-white text-weight-bold"
            >
              HTML
            </div>
          </q-card>

          <q-card class="service-card" flat bordered>
            <div class="q-pa-md">
              <q-img src="/css.png" />
            </div>
            <div
              class="text-caption text-center q-pa-sm bg-primary text-white text-weight-bold"
            >
              CSS
            </div>
          </q-card>

          <q-card class="service-card" flat bordered>
            <div class="q-pa-md">
              <q-img src="/js.png" />
            </div>
            <div
              class="text-caption text-center q-pa-sm bg-primary text-white text-weight-bold"
            >
              JAVASCRIPT
            </div>
          </q-card>

          <q-card class="service-card" flat bordered>
            <div class="q-pa-md">
              <q-img src="/typescript.png" />
            </div>
            <div
              class="text-caption text-center q-pa-sm bg-primary text-white text-weight-bold"
            >
              TYPESCRIPT
            </div>
          </q-card>

          <q-card class="service-card" flat bordered>
            <div class="q-pa-md">
              <q-img src="/bootstrap.png" />
            </div>
            <div
              class="text-caption text-center q-pa-sm bg-primary text-white text-weight-bold"
            >
              BOOTSTRAP
            </div>
          </q-card>

          <q-card class="service-card" flat bordered>
            <div class="q-pa-md">
              <q-img src="/tailwind.png" />
            </div>
            <div
              class="text-caption text-center q-pa-sm bg-primary text-white text-weight-bold q-mt-auto"
            >
              TAILWIND
            </div>
          </q-card>

          <q-card class="service-card" flat bordered>
            <div class="q-pa-md">
              <q-img src="/php.png" />
            </div>
            <div
              class="text-caption text-center q-pa-sm bg-primary text-white text-weight-bold q-mt-auto"
            >
              PHP
            </div>
          </q-card>

          <q-card class="service-card" flat bordered>
            <div class="q-pa-md">
              <q-img src="/laravel.png" />
            </div>
            <div
              class="text-caption text-center q-pa-sm bg-primary text-white text-weight-bold q-mt-auto"
            >
              LARAVEL
            </div>
          </q-card>

          <q-card class="service-card" flat bordered>
            <div class="q-pa-md">
              <q-img src="/vue.png" />
            </div>
            <div
              class="text-caption text-center q-pa-sm bg-primary text-white text-weight-bold q-mt-auto"
            >
              VUE JS
            </div>
          </q-card>

          <q-card class="service-card" flat bordered>
            <div class="q-pa-md">
              <q-img src="/nuxt.png" />
            </div>
            <div
              class="text-caption text-center q-pa-sm bg-primary text-white text-weight-bold q-mt-auto"
            >
              NUXT JS
            </div>
          </q-card>

          <q-card class="service-card" flat bordered>
            <div class="q-pa-md">
              <q-img src="/quasar.png" />
            </div>
            <div
              class="text-caption text-center q-pa-sm bg-primary text-white text-weight-bold q-mt-auto"
            >
              QUASAR
            </div>
          </q-card>

          <q-card class="service-card" flat bordered>
            <div class="q-pa-md">
              <q-img src="/mysql.png" />
            </div>
            <div
              class="text-caption text-center q-pa-sm bg-primary text-white text-weight-bold q-mt-auto"
            >
              MYSQL
            </div>
          </q-card>
        </div>
      </transition>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.service-card {
  max-width: 150px;
  width: 100%;
}
</style>
