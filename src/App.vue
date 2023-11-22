<script>
import Aside from './components/Aside.vue'
import MainBlock from './components/MainBlock.vue'

export default {
  components: {
    MainBlock,
    Aside
  },
  data() {
    return {
      headersMainBlock: [
        {
          id: 1,
          title: 'Education'
        },
        {
          id: 2,
          title: 'Achievements'
        },
        {
          id: 3,
          title: 'Tools/Skills'
        },   {
          id: 4,
          title: 'Latest projects'
        },
        {
          id: 5,
          title: 'Certificates & Awards'
        }
      ],
    }
  },
}

</script>

<template>
  <div class="container">
    <Aside />
    <div class="content">
      <MainBlock v-for="(headers, index) in headersMainBlock"
      :key="headers.id"
      :header="headers.title"     />
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
