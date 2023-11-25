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
      <div>{{ title }}</div>
    </div>
    <div class="education__cards__item__title">{{ name }}</div>
    <div class="education__cards__item__date">{{ date }}</div>
    <div class="education__cards__item__percentage">
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
  @media (max-width: 767px) {
    max-width: 100%;
  }
  &__logo {
    display: flex;
    align-items: center;
    & img {
      width: 38px;
      height: 48px;
    }
    & div {
      color: #2e2e48;
      font-size: 12px;
      font-weight: 500;
      line-height: 16px;
      padding-left: 8px;
    }
  }
  &__title {
    color: #2e2e48;
    font-size: 14px;
    font-weight: 500;
    line-height: 18px;
    margin-top: 8px;
  }
  &__date {
    color: #79819a;
    font-size: 10px;
    font-weight: 400;
    letter-spacing: 0.1px;
  }
  &__percentage {
    color: #5d5fef;

    font-size: 12px;
    font-weight: 400;
    line-height: normal;
    letter-spacing: 0.121px;
    & span {
      color: #79819a;
    }
  }
}
</style>
