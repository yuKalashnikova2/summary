<script>
import Aside from './components/Aside.vue'
import MainBlock from './components/MainBlock.vue'
import EducationSection from './components/EducationSection.vue'
import AchievementsSection from './components/AchievementsSection.vue'
import ToolsSection from './components/ToolsSection.vue'
import LatestProdjectsSection from './components/LatestProdjectsSection.vue'
import SertificateSection from './components/SertificateSection.vue'
export default {
  components: {
    MainBlock,
    Aside,
    EducationSection,
    AchievementsSection,
    ToolsSection,
    LatestProdjectsSection,
    SertificateSection,
  },
  data() {
    return {
      headersMainBlock: [
        {
          id: 1,
          title: 'Education',
          type: 1,
        },
        {
          id: 2,
          title: 'Achievements',
          type: 2,
        },
        {
          id: 3,
          title: 'Tools/Skills',
          type: 3,
        },
        {
          id: 4,
          title: 'Latest projects',
          type: 4,
        },
        {
          id: 5,
          title: 'Certificates & Awards',
          type: 5,
        },
      ],
    }
  },
}
</script>

<template>
  <div class="container">
    <Aside />
    <div class="content">
      <MainBlock
        v-for="(headers, index) in headersMainBlock"
        :key="headers.id"
        :header="headers.title"
      >
        <EducationSection :header="headers.title" v-if="headers.type == 1" />
        <AchievementsSection :header="headers.title" v-if="headers.type == 2" />
        <ToolsSection :header="headers.title" v-if="headers.type == 3" />
        <LatestProdjectsSection
          :header="headers.title"
          v-if="headers.type == 4"
        />
        <SertificateSection :header="headers.title" v-if="headers.type == 5" />
      </MainBlock>
    </div>
  </div>
</template>

<style lang="scss">
.container {
  max-width: 1198px;
  margin: 0 auto;
  display: flex;

  @media (max-width: 992px) {
    width: 100%;
    flex-direction: column;
  }
}
.content {
  height: 100%;
  padding: 32px 24px 2px 16px;
  background-color: #fff;
}
</style>
