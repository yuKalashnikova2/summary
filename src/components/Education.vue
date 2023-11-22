<script>
import ContentTitle from './ContentTitle.vue'
export default {
  components: {
    ContentTitle,
  },
}
</script>

<template>
  <div class="education">
    <ContentTitle title="Education" />

    <div class="education__cards">
      <div>я имитация карточки</div>
    </div>
  </div>
</template>

<style lang="scss">
.education {
  &__cards {
    margin-top: 16px;
    margin-bottom: 24px;
    border: 1px solid red;
  }
}
</style>
