<template>
  <div class="q-pa-lg bg-accent">
    <div class="max-width-lg">
      <transition appear enter-active-class="animated zoomIn slower">
        <div class="column items-center q-mb-xl">
          <h4 class="text-center text-primary q-mb-sm">My Projects</h4>
          <p class="text-body1 text-center border-b-secondary q-pb-sm">
            Here are some of my projects:
          </p>
        </div>
      </transition>

      <transition appear enter-active-class="animated slideInUp slower">
        <div class="row justify-center q-gutter-md">
          <q-card class="service-card q-pa-md">
            <q-img src="/attendance.PNG" height="200px" class="border" />

            <q-card-section>
              <div class="text-h6">Attendance Monitoring</div>
              <div class="text-subtitle2">A Project Creation</div>
            </q-card-section>

            <q-card-section class="q-pt-none q-mb-xl">
              Attendance monitoring system is all about tracking the trainee's
              attendance during the training. Through seamless integration with
              databases and automated report generation, it provides trainers
              and administrators with valuable insights into attendance
              patterns.
            </q-card-section>

            <q-card-actions align="center" class="absolute-bottom q-pa-lg">
              <q-btn color="secondary">Visit Site</q-btn>
            </q-card-actions>
          </q-card>

          <q-card class="service-card q-pa-md">
            <q-img src="/mycampusmate.PNG" height="200px" class="border" />

            <q-card-section>
              <div class="text-h6">My Campus Mate</div>
              <div class="text-subtitle2">A Social Media website</div>
            </q-card-section>

            <q-card-section class="q-pt-none q-mb-xl">
              This project offers users a personalized platform for social
              interaction and content sharing. With a user-friendly interface
              and customizable profiles, individuals can connect with friends,
              share updates, photos, and engage communication through chat,
              comments and likes.
            </q-card-section>

            <q-card-actions align="center" class="absolute-bottom q-pa-lg">
              <q-btn color="secondary">Visit Site</q-btn>
            </q-card-actions>
          </q-card>

          <q-card class="service-card q-pa-md">
            <q-img src="/natours.PNG" height="200px" class="border" />

            <q-card-section>
              <div class="text-h6">Natours</div>
              <div class="text-subtitle2">A Nature website</div>
            </q-card-section>

            <q-card-section class="q-pt-none q-mb-xl">
              Introducing a captivating travel and nature website, a digital
              gateway to explore the world's natural wonders. This platform is
              designed to inspire adventure and appreciation for the great
              outdoors, offering a curated collection of breathtaking
              destinations, eco-friendly travel tips, and immersive experiences
              in nature.
            </q-card-section>

            <q-card-actions align="center" class="absolute-bottom q-pa-lg">
              <q-btn color="secondary">Visit Site</q-btn>
            </q-card-actions>
          </q-card>

          <q-card class="service-card q-pa-md">
            <q-img src="/assessment.PNG" height="200px" class="border" />

            <q-card-section>
              <div class="text-h6">Teacher Tribe</div>
              <div class="text-subtitle2">A coding assessment website</div>
            </q-card-section>

            <q-card-section class="q-pt-none q-mb-xl">
              A coding assessment website designed to empower developers and
              tech enthusiasts alike. It offers a comprehensive suite of
              assessments designed to sharpen coding skills and assess
              proficiency in HTML, CSS, and Javascript.
            </q-card-section>

            <q-card-actions align="center" class="absolute-bottom q-pa-lg">
              <q-btn color="secondary">Visit Site</q-btn>
            </q-card-actions>
          </q-card>

          <q-card class="service-card q-pa-md">
            <q-img src="/elearning.PNG" height="200px" class="border" />

            <q-card-section>
              <div class="text-h6">Teacher Tribe - Elearning</div>
              <div class="text-subtitle2">
                An interactive coding learning website
              </div>
            </q-card-section>

            <q-card-section class="q-pt-none q-mb-xl">
              This website is a dynamic hub for learners passionate about
              programming. With an intuitive user interface and adaptive
              difficulty levels, users can embark on personalized learning
              journeys tailored to their skill levels and learning objectives.
            </q-card-section>

            <q-card-actions align="center" class="absolute-bottom q-pa-lg">
              <q-btn color="secondary">Visit Site</q-btn>
            </q-card-actions>
          </q-card>
        </div>
      </transition>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.service-card {
  max-width: 380px;
  width: 100%;
}

.border {
  border: 1px solid #b9b9b9;
}
</style>
