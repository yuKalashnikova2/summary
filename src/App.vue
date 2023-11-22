<script setup>
import Aside from './components/Aside.vue'
import ContentTitle from './components/ContentTitle.vue';
</script>

<template>
  <div class="container">
    <Aside />
    <div class="content">
      <ContentTitle title="Education" />
    </div>
  </div>
</template>

<style lang="scss">
.container {
  max-width: 594px;
  margin: 0 auto;
  display: flex;

  @media (max-width: 577px) {
    width: 100%;
    flex-direction: column;
  }
}
.content {
  padding: 32px 24px 2px 16px;
  background-color: #FFF;
}
</style>
