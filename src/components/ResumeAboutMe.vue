<template>
  <div class="about-me">

    <h2 class="about-me__title">Обо мне</h2>

    <ul class="about-me__list">
      <li class="about-me__list-item">Более 3-х лет занимаюсь разработкой</li>

      <li class="about-me__list-item">Принимал участие во множестве проектов</li>

      <li class="about-me__list-item">Имею опыт работы в компании и на фрилансе</li>

      <li class="about-me__list-item">Работал единственным разработчиком на проекте</li>

      <li class="about-me__list-item">Быстро учусь и осваиваю новые технологии</li>

      <li class="about-me__list-item">Всегда легко нахожу общий язык с коллегами</li>

      <li class="about-me__list-item">Люблю фронтенд - потому что это красиво </li>
    </ul>

  </div>
</template>

<style scoped lang="scss">
.about-me {
  width: 100%;
  height: 100%;
  margin: 200px 0;
  border-left: 4px solid $black-light;
  padding-left: 32px;

  &__title {
    margin-bottom: 24px;
  }

  &__list {
    display: flex;
    flex-direction: column;
    gap: 30px;
    font-size: 24px;
    font-weight: 400;

    &-item {
      display: flex;
      align-items: center;

      &::before {
        content: "";
        display: block;
        width: 8px;
        height: 8px;
        background-color: $accent;
        margin-right: 8px;
      }
    }
  }
}
</style>