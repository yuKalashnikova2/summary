<script>
export default {
  props: {
    title: String,
    name: String,
    date: String,
    percentage: Number,
    images: String,
  },
}
</script>

<template>
  <div class="education__cards__item">
    <div class="education__cards__item__logo">
      <img :src="'/assets/svg/' + images + '.svg'" :alt="images" />
      <div class="subtitle subtitle_black">{{ title }}</div>
    </div>
    <div class="subtitle-text education__cards__item__title">{{ name }}</div>
    <div class="subtitle education__cards__item__date">{{ date }}</div>
    <div class="subtitle education__cards__item__percentage">
      Percentage - <span> {{ percentage }}%</span>
    </div>
  </div>
</template>

<style lang="scss">
.education__cards__item {
  background-color: #f7f9fc;
  border-radius: 8.067px 0px 0px 8.067px;
  padding: 16px 24px;
  max-width: 180px;
  @media (max-width: 992px) {
    max-width: 100%;
  }
  &__logo {
    display: flex;
    align-items: center;
    gap: 16px;
    & img {
      width: 38px;
      height: 48px;
    }

  }
  &__title {
    color: #2e2e48;
  }
  &__date {
    color: #79819a;
  }
  &__percentage {
    color: #5d5fef;
    letter-spacing: 0.121px;
    & span {
      color: #79819a;
    }
  }
}
</style>
