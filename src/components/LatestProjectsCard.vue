<script>
export default {
  props: {
    title: String,
    description: String,
    image: String,
    link: String,
  },
}
</script>
<template>
  <div class="latest-projects__cards__item">
    <div class="latest-projects__cards__item-top">
      <div class="latest-projects__cards__item-top__logo">
        <img :src="'src/assets/svg/tools/' + image + '.svg'" :alt="image" />
      </div>

      <div class="latest-projects__cards__item-top__description">
        <div
          class="latest-projects__cards__item-top__description-title subtitle-text subtitle-text_black subtitle-text_medium"
        >
          {{ title }}
        </div>
        <div class="subtitle subtitle_font-medium">{{ description }}</div>
      </div>
    </div>
    <div class="latest-projects__cards__item-link">
      <div>
        <img src="../assets/svg/link.svg" alt="link" />
      </div>
      <a :href="link" class="latest-projects__cards__item-link__text underline">
        {{ link }}
      </a>
    </div>
  </div>
</template>

<style lang="scss">
.latest-projects__cards__item {
  background-color: #f7f9fc;
  padding: 12px;
  border-radius: 4px 0px 0px 4px;
  max-width: 170px;
  @media (max-width: 577px) {
    max-width: 100%;
  }
  &-top {
    display: flex;
    gap: 8px;
    &__logo {
      & img {
        width: 24px;
        height: 24px;
        border-radius: 8px;
      }
    }
    &__description {
      &-title {
        margin-bottom: 2px;
      }
    }
  }
  &-link {
    display: flex;
    align-items: center;
    gap: 6px;
    align-self: stretch;
    &__text {
      color: #516cf7;
      font-family: 'Outfit', sans-serif;
      font-size: 8px;
      font-weight: 600;
      line-height: 10px;
    }
  }
}
</style>
