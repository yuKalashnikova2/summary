<script>
export default {
  props: {
    isCard: Boolean,
  },
}
</script>

<template>
  <div class="divider__block">
    <div
      :class="['divider__block__circle', isCard ? 'divider__card__circle' : '']"
    >
      <div
        :class="[
          'divider__block__circle__inside',
          isCard ? 'divider__card__circle__inside' : '',
        ]"
      >
        <!-- <img src="/assets/svg/circle-inside-card.svg" alt="" v-if="isCard" />
        <img src="/assets/svg/circle-inside.svg" alt="circle" v-else /> -->
        <div class="divider__card__circle__inside-black" v-if="isCard"></div>
        <div class="divider__block__circle__inside-violet" v-else></div>
      </div>
    </div>

    <div
      :class="['divider__block__band', isCard ? 'divider__card__band' : '']"
    ></div>
  </div>
</template>

<style lang="scss">
.divider__block {
  display: flex;
  flex-direction: column;
  align-items: center;
  @media (max-width: 992px) {
    display: none;
  }
  &__circle {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 32px;
    height: 32px;
    border-radius: 100px;
    background: #fff;
    box-shadow: 0px 1px 1px 0px rgba(0, 0, 0, 0.04) inset,
      0px 6px 24px 0px rgba(0, 0, 0, 0.04), 0px 1px 4px 0px rgba(0, 0, 0, 0.05);
    &__inside {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 20px;
      height: 20px;
      flex-shrink: 0;
      border-radius: 100%;
      &-violet {
        width: 9px;
        height: 9px;
        background-color: #5531a7;
        border-radius: 100%;
      }
    }
  }
  &__band {
    height: 100vh;
    width: 1px;
    flex: 1 0 0;
    background-color: #e2e6ee;
  }
}

.divider__card {
  &__circle {
    box-shadow: none;
    &__inside {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 15px;
      height: 15px;
      &-black {
        width: 6px;
        height: 6px;
        border-radius: 100%;
        background-color: #2e2e48;
      }
    }
  }
  &__band {
    background-color: #f7f9fc;
  }
}
</style>
