<template>
  <div class="projects">

    <div class="projects__wrapper">
      <h2 class="projects__title">Проекты</h2>
      <div class="projects__list">
        <a class="projects-card" v-for=" project of  projects " :href="project.link" target="_blank">
          <div class="projects-card__img">
            <img :src="resolveImgPath(project.img)" :alt="'Скриншот главной страницы ' + project.name">
          </div>
          <div class="projects-card__name">
            {{ project.name }}
          </div>
          <div class="projects-card__stack">
            <span :class="classes(i)" v-for=" i  of  project.stack ">{{ i }}</span>
          </div>
        </a>
      </div>
    </div>

    <div class="projects__wrapper">
      <h2 class="projects__title">Пример кода</h2>
      <div class="projects__list">
        <a class="projects-card" v-for="  project  of  myProjects " :href="project.link" target="_blank">
          <div class="projects-card__img">
            <img :src="resolveImgPath(project.img)" :alt="project.imgAlt + project.name">
          </div>
          <div class="projects-card__name">
            {{ project.name }}
          </div>
          <div class="projects-card__stack">
            <span :class="classes(i)" v-for=" i  of  project.stack ">{{ i }}</span>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script setup>

import { computed } from 'vue'

const projects = [
  {
    link: 'https://vityaz.aero/',
    img: 'vityaz.webp',
    name: 'Vityaz-aero',
    stack: ['Vue', 'TypeScript', 'SCSS']
  },
  {
    link: 'https://rtg-company.ru/',
    img: 'rtg.webp',
    name: 'Rtg',
    stack: ['JavaScript', 'CSS', 'HTML']
  },
  {
    link: 'https://qpzip.ru/',
    img: 'qpzip.webp',
    name: 'Qp-zip',
    stack: ['JavaScript', 'CSS', 'HTML']
  },
  {
    link: 'https://poisktenderov.ru/',
    img: 'poisktenderov.webp',
    name: 'Poisktenderov',
    stack: ['PUG', 'JavaScript', 'SCSS']
  },
  {
    link: 'https://kamon.dance/',
    img: 'kamon.webp',
    name: 'Kamon',
    stack: ['Vue', 'JavaScript', 'SCSS']
  },

]

const myProjects = [
  {
    link: 'https://github.com/DWNMRS/',
    img: 'github.webp',
    name: 'GitHub',
    stack: []
  },
  {
    link: 'https://dwnmrs.github.io/movee',
    img: 'movee.webp',
    name: 'Movee',
    stack: ['Vue', 'TypeScript', 'SCSS', 'Vite']
  },
  {
    link: 'https://dwnmrs.github.io/search',
    img: 'search.webp',
    name: 'Search',
    stack: ['Nuxt', 'TypeScript', 'SCSS']
  },

]

const classes = computed(() => (i) => {
  return {
    'projects-card__stack-item': true,
    'projects-card__stack-item--vue': i === 'Vue' || i === 'Nuxt',
    'projects-card__stack-item--scss': i === 'SCSS',
    'projects-card__stack-item--html': i === 'HTML',
    'projects-card__stack-item--ts': i === 'TypeScript',
    'projects-card__stack-item--js': i === 'JavaScript',
    'projects-card__stack-item--pug': i === 'PUG',
    'projects-card__stack-item--css': i === 'CSS',
    'projects-card__stack-item--vite': i === 'Vite',
  }
})


const resolveImgPath = (img) => {
  return new URL(`../assets/images/${img}`, import.meta.url).href;
}

</script>

<style scoped lang="scss">
.projects {
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 200px;
  margin: 200px 0;

  @include break-md {
    margin: 140px 0;
    gap: 140px;
  }

  @include break-md {
    margin: 80px 0;
    gap: 80px;
  }

  &__title {
    margin-bottom: 56px;
  }

  &__list {
    display: flex;
    flex-wrap: wrap;
    gap: 56px 32px;
  }

  &-card {
    width: calc((100% / 3) - 22px);
    height: auto;

    @include break-md {
      width: calc((100% / 2) - 16px);
    }
    @include break-sm {
      width: 100%;
    }

    &__name {
      font-size: 20px;
      font-weight: 600;
      margin: 16px 0;
    }

    &__img {
      width: 100%;
      height: 200px;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;


      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        transition: 0.4s;

        &:hover {
          width: 110%;
          height: 110%;
        }
      }
    }

    &__stack {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;

      &-item {
        font-size: 16px;
        font-weight: 400;
        line-height: 16px;
        color: $white;
        padding: 8px 12px;

        &--pug {
          background-color: #a86454;
        }

        &--js {
          background-color: #cfa900;
        }

        &--ts {
          background-color: #3178C6;
        }

        &--css {
          background-color: #264DE4;
        }

        &--vue {
          background-color: #41B883;
        }

        &--scss {
          background-color: #CD6799;
        }

        &--html {
          background-color: #F16529;
        }

        &--vite {
          background: linear-gradient(#41D1FF, #BD34FE);
        }
      }
    }
  }
}
</style>