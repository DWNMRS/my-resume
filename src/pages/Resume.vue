<template>
  <div class="resume">

    <ResumeGreetings />

    <ResumeAboutMe />

    <ResumeSkills />

    <ResumeProjects />

    <ResumeFooter/>
  </div>
</template>

<script setup>
import ResumeGreetings from '../components/ResumeGreetings.vue'
import ResumeAboutMe from '../components/ResumeAboutMe.vue'
import ResumeSkills from '../components/ResumeSkills.vue'
import ResumeProjects from '../components/ResumeProjects.vue'
import ResumeFooter from '../components/ResumeFooter.vue'
</script>

<style lang="scss">
.resume {
  margin: 0 auto;
  padding: 0 32px;
  width: 100%;
  max-width: 1200px;
}
</style>
