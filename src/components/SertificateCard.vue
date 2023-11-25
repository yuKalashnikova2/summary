<script>
export default {
  props: {
    title: String,
    subtitle: String,
    date: String,
    location: String,
    image: String,
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

<style lang="scss">
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
      gap: 4px;
    }
  }
}
</style>
