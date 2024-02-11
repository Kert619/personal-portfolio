<template>
  <div class="q-pa-lg">
    <div class="max-width-lg">
      <transition appear enter-active-class="animated zoomIn slower">
        <div class="column items-center">
          <h4 class="text-center text-primary q-mb-sm">Education</h4>
          <p class="text-body1 text-center border-b-secondary q-pb-sm">
            My education timeline:
          </p>
        </div>
      </transition>

      <transition appear enter-active-class="animated fadeInLeft slower">
        <div class="q-px-lg q-py-md">
          <q-timeline color="secondary" layout="loose">
            <q-timeline-entry title="Elementary" subtitle="2007 - 2013">
              <div>Tomongtong Elementary School</div>
              <div class="text-caption text-weight-bold">Grade 1 - Grade 6</div>
            </q-timeline-entry>

            <q-timeline-entry title="Junior High School" subtitle="2013 - 2017">
              <div>E.B Magalona National High School</div>
              <div class="text-caption text-weight-bold">
                Grade 7 - Grade 10
              </div>
            </q-timeline-entry>

            <q-timeline-entry title="Senior High School" subtitle="2017 - 2019">
              <div>E.B Magalona National High School</div>
              <div class="text-caption text-weight-bold">
                Grade 11 - Grade 12
              </div>
              <div class="text-caption text-weight-bold">
                TVL - Computer Systems Servicing
              </div>
            </q-timeline-entry>

            <q-timeline-entry title="College" subtitle="2019 - 2023">
              <div>Carlos Hilado Memorial State University</div>
              <div class="text-caption text-weight-bold">
                1st Year - 4th Year
              </div>
              <div class="text-caption text-weight-bold">
                Bachelor of Science in Information Systems
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
