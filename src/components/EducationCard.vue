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
      <img :src="'src/assets/svg/' + images + '.svg'" :alt="images" />
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
  padding: 8px 12px;
  &__logo {
    display: flex;
    align-items: center;
    & img {
      width: 19px;
      height: 24px;
    }
    & div {
      color: #2e2e48;
      font-size: 6px;
      font-weight: 500;
      line-height: 8px;
      padding-left: 8px;
    }
  }
  &__title {
    color: #2e2e48;
    font-size: 7px;
    font-weight: 500;
    line-height: 9px;
    margin-top: 4px;
  }
  &__date {
    color: #79819a;
    font-size: 5px;
    font-weight: 400;
    letter-spacing: 0.05px;
  }
  &__percentage {
    color: #5d5fef;

    font-size: 6px;
    font-weight: 400;
    line-height: normal;
    letter-spacing: 0.06px;
    & span {
      color: #79819a;
    }
  }
}
</style>
