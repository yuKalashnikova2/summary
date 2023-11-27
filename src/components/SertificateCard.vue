<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Title',
    },
    subtitle: {
      type: String,
      required: true,
    },
    date: {
      type: String,
      required: false,
    },
    location: {
      type: String,
      required: false,
    },
    image: {
      type: String,
      required: false,
    },
  },
}
</script>
<template>
  <div class="sertifiacate__cards__item">
    <div class="sertifiacate__cards__item-logo">
      <div class="sertifiacate__cards__item-logo__img">
        <img :src="'/assets/svg/tools/' + image + '.svg'" :alt="image" />
      </div>
      <div class="sertifiacate__cards__item-logo__text">
        <div class="subtitle">{{ title }}</div>
        <div class="subtitle-text subtitle-text_black">
          {{ subtitle }}
        </div>
      </div>
    </div>

    <div class="sertifiacate__cards__item-info">
      <div class="subtitle_font-small subtitle_font-small_dark">
        {{ date }}
      </div>
      <div class="sertifiacate__cards__item-info__location">
        <img
          width="12"
          height="12"
          src="/assets/svg/location.svg"
          alt="location"
        />
        <div class="subtitle_font-small">{{ location }}</div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.sertifiacate__cards__item {
  padding: 16px 24px;
  display: flex;
  background-color: #f7f9fc;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  &-logo {
    display: flex;
    & > *:not(:last-child) {
      margin-right: 12px;
    }
    &__img {
      width: 45px;
      height: 45px;
    }
    &__text {
      display: flex;
      flex-direction: column;
    }
  }

  &-info {
    display: flex;
    flex-direction: column;
    gap: 4px;
    &__location {
      display: flex;
      align-items: center;
      gap: 4px;
    }
    @media (max-width: 767px) {
      display: none;
    }
  }
}
</style>
