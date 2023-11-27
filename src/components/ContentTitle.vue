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
  font-size: 24px;
  font-style: normal;
  font-weight: 500;
  line-height: 32px;
  letter-spacing: 0.242px;
  @media (max-width: 992px) {
    text-align: center;
  }
}
</style>
