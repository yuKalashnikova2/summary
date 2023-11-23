<script>
export default {
  props: {
    title: String,
  },
}
</script>

<template>
  <h2 class="content__title">{{ title }}</h2>
</template>

<style lang="scss">
.content__title {
  color: #2e2e48;
  font-family: 'Outfit', sans-serif;
  font-size: 12px;
  font-style: normal;
  font-weight: 500;
  line-height: 16px;
  letter-spacing: 0.12px;
  @media (max-width: 577px) {
    text-align: center;
  }
}
</style>
