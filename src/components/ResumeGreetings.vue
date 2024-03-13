<template>
  <div class="greetings">

    <div class="greetings__text">
      <h1>Привет!</h1>
      <span>Меня зовут <b>Егор</b>, я</span>
      <span class="greetings__accent">Frontend-разработчик</span>

      <div class="greetings__buttons">

        <a href="/my-resume/documents/resume.pdf" target="_blank" class="greetings__btn">
          Скачать резюме
          <AppIcon class="greetings__icon" :width="24" :height="24" :name="'Resume'" />
        </a>

        <a href="https://t.me/downmars" target="_blank" class="greetings__btn">
          Написать мне
          <AppIcon class="greetings__icon" :width="24" :height="24" :name="'Telegram'" />
        </a>

      </div>
    </div>

    <div class="greetings__photo">
      <img class="greetings__photo-img" src="../assets/images/i2.webp">
    </div>
  </div>
</template>

<script setup>
import AppIcon from '@/assets/icons/AppIcon.vue'
</script>

<style scoped lang="scss">
.greetings {
  display: flex;
  justify-content: space-between;
  gap: 32px;
  margin: 200px 0;

  &__text {
    display: flex;
    flex-direction: column;
    gap: 24px;
    border-left: 4px solid $black-light;
    padding-left: 32px;
    font-size: 40px;
  }

  &__accent {
    background: $accent;
    color: $black;
    padding: 10px 20px;
    font-weight: 900;
  }

  &__photo {
    width: 350px;
    height: 100%;
    overflow: hidden;
    background-color: grey;

    &-img {
      width: 100%;
      object-fit: contain;
    }
  }

  &__buttons {
    display: flex;
    gap: 32px;
  }

  &__btn {
    border: 1px solid $transparent;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 4px 8px;
    font-size: 18px;
    font-weight: 300;
    color: $white;
    cursor: pointer;
    transition: 0.2s;

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