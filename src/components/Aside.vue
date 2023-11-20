<template>
  <div class="aside">
    <header class="aside__header">
      <img src="../assets/logo.png" alt="logo" class="aside__header-logo" />
      <h1 class="aside__header-title">Yuliya Kalashnikova</h1>
    </header>

    <p class="aside__about">
      A well-organized, creative and goaloriented graduate possessing excellent
      communication, problem-solving and leadership skills with a flair to
      explore Computer Science Engineering
    </p>
  </div>
</template>

<style lang="scss">
.aside {
  display: flex;
  flex-direction: column;
  background-color: #f7fcff;
  width: 176px;
  padding: 24px 4px 0 24px;

  &__header {
    margin-bottom: 16px;
    &-logo {
      border-radius: 100%;
      width: 48px;
      height: 48px;
    }
    &-title {
      font-size: 16px;
      font-weight: 500;
      line-height: 20px;
      letter-spacing: -2%;
      color: #2e2e48;
      padding-top: 8px;
    }
  }

  &__about {
    font-size: 9px;
    font-weight: 500;
    color: #47516b;
    letter-spacing: 2%;
    line-height: 12px;
    padding-bottom: 4px;
  }
}
</style>
