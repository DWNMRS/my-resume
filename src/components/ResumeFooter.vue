<template>
  <div class="footer">
    <a href="/my-resume/documents/resume.pdf" target="_blank" class="footer__btn">
      Скачать&nbsp;резюме
      <AppIcon class="footer__icon" :width="24" :height="24" :name="'Resume'" />
    </a>

    <a href="https://t.me/downmars" target="_blank" class="footer__btn">
      Написать&nbsp;мне
      <AppIcon class="footer__icon" :width="24" :height="24" :name="'Telegram'" />
    </a>
  </div>
</template>

<script setup>
import AppIcon from '@/assets/icons/AppIcon.vue'
</script>

<style scoped lang="scss">

.footer {
  padding-top: 32px;
  padding-bottom: 100px;
  border-top: 2px solid $black-light;
  width: 100%;
  display: flex;
  justify-content: center;
  gap: 32px;

  @include break-lg {
      gap: 24px;
    }

    @include break-md {
      gap: 16px;
      padding: 16px 0;
    }

    @include break-sm {
      justify-content: space-between;
    }

  &__btn {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 4px 8px;
    font-size: 18px;
    font-weight: 300;
    color: $white;
    cursor: pointer;
    transition: 0.2s;

    @include break-sm {
      font-size: 12px;
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