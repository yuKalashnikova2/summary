<script>
import Divider from './Divider.vue'
export default {
  data() {
    return {
      isCard: true,
    }
  },
  props: {
    subtitle: String,
    title: String,
    date: String,
    decription: String,
    logo: String,
  },
  components: {
    Divider,
  },
}
</script>
<template>
  <div class="achievements__cards__item">
    <Divider :isCard="isCard" />
    <div class="achievements__cards__item-content">
      <div class="achievements__cards__item-content__experience">
        <div class="achievements__cards__item-content__experience-date">
          <div class="subtitle_font-small subtitle_font-small_dark">
            {{ date }}
          </div>
          <div
            class="achievements__cards__item-content__experience-date__online"
          >
            <img
              width="12"
              height="12"
              src="/assets/svg/location.svg"
              alt="location"
            />
            <div class="subtitle_font-small">Online</div>
          </div>
        </div>

        <div class="achievements__cards__item-content__experience-title">
          <img
            :src="'/assets/svg/social/' + logo + '.svg'"
            :alt="logo"
            class="achievements__cards__item-content__experience-title__img"
            width="50"
            height="50"
          />
          <div
            class="achievements__cards__item-content__experience-title__text"
          >
            <div class="subtitle">{{ subtitle }}</div>
            <div class="subtitle-text subtitle-text_black">{{ title }}</div>
          </div>
        </div>
      </div>

      <div class="achievements__cards__item-content__description">
        <p class="subtitle_font-small">
          {{ decription }}
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.achievements__cards__item {
  display: flex;
  & > *:not(:last-child) {
    margin-right: 8px;
  }
  @media (max-width: 767px) {
    background-color: #f7f9fc;
  }
  &-content {
    display: flex;
    justify-content: space-between;
    @media (max-width: 767px) {
      padding: 15px;
    }
    &__experience {
      display: flex;
      flex-direction: column;
      flex-shrink: 0;
      gap: 4px;

      &-date {
        display: flex;
        gap: 8px;
        &__online {
          display: flex;
          & > *:not(:last-child) {
            margin-right: 2px;
          }
        }
      }
      &-title {
        display: flex;
        align-items: center;
        gap: 4px;
        align-self: stretch;
        &__text {
          display: flex;
          flex-direction: column;
          gap: 8px;
        }
        &__img {
          width: 50px;
          height: 50px;
          margin-right: 16px;
        }
      }
    }
    &__description {
      padding-left: 30px;
    }
    @media (max-width: 767px) {
      flex-direction: column;
      gap: 10px;
    }
  }
}
</style>
