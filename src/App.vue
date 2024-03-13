<template>
  <Resume />
  <AppIconSprite />
</template>

<script setup>
import Resume from './pages/Resume.vue';
import AppIconSprite from "@/assets/icons/AppIconSprite/AppIconSprite.vue"
</script>

<style lang="scss">
body {
  background: $black;

  &::-webkit-scrollbar {
    background-color: $transparent;
    width: 14px;

    &-thumb {
      width: 4px;
      border-radius: 2px;
      background-color: #FFFFFF14;
    }
  }
}

#app {
  margin: 0 auto;
  width: 100%;
  color: $text;
  overflow: hidden;
  font-family: "Unbounded", sans-serif;
}
</style>
