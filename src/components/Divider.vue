<template>
  <div class="divider__block">
    <div class="divider__block__circle">
      <div class="divider__block__circle__inside">
        <img src="../assets/svg/circle-inside.svg" alt="circle" />
      </div>
    </div>

    <div class="divider__block__band"></div>
  </div>
</template>

<style lang="scss">
.divider__block {
  display: flex;
  flex-direction: column;
  align-items: center;
  &__circle {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 16px;
    height: 16px;
    border-radius: 100px;
    background: #fff;
    box-shadow: 0px 1px 1px 0px rgba(0, 0, 0, 0.04) inset,
      0px 6px 24px 0px rgba(0, 0, 0, 0.04), 0px 1px 4px 0px rgba(0, 0, 0, 0.05);
    &__inside {
      width: 10px;
      height: 10px;
      flex-shrink: 0;
      border-radius: 100%;
    }
  }
  &__band {
    height: 100vh;
    width: 0.5px;
    flex: 1 0 0;
    background-color: #e2e6ee;
  }
}
</style>
