<template>
  <div class="skills">
    <h2 class="skills__title">Мой стек:</h2>
    <div class="skills__list">
      <div class="skills__item" v-for="skill of skills">
        <AppIcon class="skills__icon" :width="skill === 'Gulp' ? 32 : 64" :height="64" :name="`${skill}`" />
        <span>{{ skill }}</span>
      </div>
    </div>
  </div>
</template>

<script setup>
import AppIcon from '@/assets/icons/AppIcon.vue'
const skills = ['Vue2/3', 'Nuxt2/3', 'VueX', 'Pinia', 'Vite', 'Webpack', 'Gulp', 'TypeScript', 'JavaScript', 'SCSS', 'CSS', 'HTML']
</script>

<style scoped lang="scss">
.skills {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 100%;
  height: 100%;
  margin: 200px 0;

  &__title {
    margin-bottom: 56px;
  }

  &__list {
    font-size: 24px;
    display: flex;
    flex-wrap: wrap;
    gap: 56px;
  }

  &__item {
    display: flex;
    align-items: center;
    text-align: center;
  }

  &__icon {
    width: 32px;
    height: 32px;
    margin-right: 16px;
  }
}
</style>