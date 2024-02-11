<template>
  <div class="q-pa-lg bg-accent">
    <div class="max-width-lg">
      <transition appear enter-active-class="animated zoomIn slower">
        <div class="column items-center">
          <h4 class="text-center text-primary q-mb-sm">Experiences</h4>
          <p class="text-body1 text-center border-b-secondary q-pb-sm">
            My experiences timeline:
          </p>
        </div>
      </transition>

      <transition appear enter-active-class="animated fadeInLeft slower">
        <div class="q-px-lg q-py-md">
          <q-timeline color="secondary" layout="loose">
            <q-timeline-entry
              title="Software Development Training Program - OJT"
              subtitle="Mar 2023 - Aug 2023"
            >
              <div>
                Negros Occidental Language in Information Technology Center
              </div>
              <div class="text-caption text-weight-bold">- Best Programmer</div>
              <div class="text-caption text-weight-bold">
                - Top Scorer Awardee During Assessment
              </div>
              <div class="text-caption text-weight-bold">
                - Best Team Project
              </div>
            </q-timeline-entry>

            <q-timeline-entry
              title="Full Stack Developer"
              subtitle="Sept 2023 - Feb 2024"
            >
              <div>Coders Tribe</div>
              <div class="text-caption text-weight-bold">
                - User Interface Design
              </div>
              <div class="text-caption text-weight-bold">
                - Responsive Design
              </div>
              <div class="text-caption text-weight-bold">
                - Database Management
              </div>
              <div class="text-caption text-weight-bold">
                - REST API Development
              </div>
            </q-timeline-entry>
          </q-timeline>
        </div>
      </transition>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss"></style>
