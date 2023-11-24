<script>
export default {
  props: {
    name: String,
    image: String,
    description: String,
  },
}
</script>

<template>
  <div class="tools__cards__item">
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
  padding: 8px;
  background-color: #f7f9fc;

  &-logo {
    width: 24px;
    height: 24px;
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
