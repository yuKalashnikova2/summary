<script>
export default {
  props: {
    name: String,
    image: String,
    description: String,
    isTools: Boolean,
  },
}
</script>

<template>
  <div
    :class="[
      'tools__cards__item',
      isTools ? 'tools__cards__item-tools' : 'tools__cards__item-skills',
    ]"
  >
    <div class="tools__cards__item-logo">
      <img :src="'/assets/svg/tools/' + image + '.svg'" :alt="image" />
    </div>

    <div class="tools__cards__item-text">
      <div class="subtitle-text subtitle-text_black">{{ name }}</div>
      <div class="subtitle">{{ description }}</div>
    </div>
  </div>
</template>

<style lang="scss">
.tools__cards__item {
  padding: 16px;
  background-color: #f7f9fc;
  &-tools {
    min-width: 277px;
  }
  &-skills {
    min-width: 133px;
  }
  &-logo {
    width: 48px;
    height: 48px;
    margin: 0 auto;
    margin-bottom: 4px;
    img {
      object-fit: cover;
      max-width: 100%;
      max-height: 100%;
    }
  }
  &-text {
    text-align: center;
  }
}
</style>
