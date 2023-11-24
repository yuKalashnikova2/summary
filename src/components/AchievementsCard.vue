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
              width="6"
              height="6"
              src="../assets/svg/location.svg"
              alt="location"
            />
            <div class="subtitle_font-small">Online</div>
          </div>
        </div>

        <div class="achievements__cards__item-content__experience-title">
          <img
            :src="'./src/assets/svg/social/' + logo + '.svg'"
            :alt="logo"
            class="achievements__cards__item-content__experience-title__img"
            width="25"
            height="25"
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
  @media (max-width: 577px) {
    background-color: #F7F9FC;

  }
  &-content {
    display: flex;
    & > *:not(:last-child) {
      margin-right: 4px;
      padding: 3px 0 8px 0;
    }
    &__experience {
      display: flex;
      min-width: 120px;
      flex-direction: column;
      gap: 4px;

      &-date {
        display: flex;
        & > *:not(:last-child) {
          margin-right: 2px;
        }
        margin-bottom: 4px;
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
        gap: 2px;
        align-self: stretch;
        &__text {
          display: flex;
          flex-direction: column;
          gap: 2px;
        }
        &__img {
          width: 25px;
          height: 25px;
          margin-right: 8px;
        }
      }
    }
    @media (max-width: 577px) {
      flex-direction: column;
    }
  }
}
</style>
