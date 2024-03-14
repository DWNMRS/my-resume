<template>
  <div class="greetings">

    <div class="greetings__text">
      <h1>Привет!</h1>
      <span>Меня зовут <b>Егор</b>, я</span>
      <span class="greetings__accent">Frontend-разработчик</span>

      <div class="greetings__buttons">

        <a href="/my-resume/documents/resume.pdf" target="_blank" class="greetings__btn">
          Скачать&nbsp;резюме
          <AppIcon class="greetings__icon" :width="24" :height="24" :name="'Resume'" />
        </a>

        <a href="https://t.me/downmars" target="_blank" class="greetings__btn">
          Написать&nbsp;мне
          <AppIcon class="greetings__icon" :width="24" :height="24" :name="'Telegram'" />
        </a>

      </div>
    </div>

    <div class="greetings__photo">
      <img class="greetings__photo-img" src="../assets/images/i.webp">
    </div>
  </div>
</template>

<script setup>
import AppIcon from '@/assets/icons/AppIcon.vue'
</script>

<style scoped lang="scss">
.greetings {
  display: flex;
  gap: 32px;
  margin: 200px 0;

  @include break-lg {
    gap: 24px;
  }

  @include break-md {
    gap: 16px;
    margin: 140px  0;
  }

  @include break-sm {
    gap: 8px;
    margin: 80px  0;
  }

  &__text {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 24px;
    border-left: 4px solid $black-light;
    padding-left: 32px;
    font-size: 40px;

    @include break-xl {
      font-size: 32px;
    }

    @include break-lg {
      font-size: 24px;
    }

    @include break-md {
      font-size: 16px;
      padding-left: 0;
      border-left: none;
      gap: 16px;
    }

  }

  &__accent {
    background: $accent;
    color: $black;
    padding: 10px 20px;
    font-weight: 900;
    width: fit-content;

    @include break-md {
      padding: 4px 8px;
    }
  }

  &__photo {
    width: 350px;

    &-img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }

  &__buttons {
    display: flex;
    gap: 32px;

    @include break-lg {
      gap: 24px;
    }

    @include break-md {
      gap: 16px;
      flex-direction: column;
    }

    @include break-sm {
      gap: 8px;
    }
  }

  &__btn {
    border: 1px solid $transparent;
    display: flex;
    align-items: center;
    font-size: 18px;
    font-weight: 300;
    color: $white;
    cursor: pointer;
    transition: 0.2s;

    @include break-lg {
      font-size: 16px;
    }

    &:hover {
      color: $accent;
    }
  }

  &__icon {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-left: 8px;
  }
}
</style>