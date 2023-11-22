<script>
import ContentTitle from './ContentTitle.vue'
import Divider from './Divider.vue'
import EducationCard from './EducationCard.vue'
export default {
  components: {
    ContentTitle,
    EducationCard,
    Divider
  },
  props: {
    header: String,
  },
}
</script>

<template>
  <div class="main__block">
    <Divider />
    <div class="education">
      <ContentTitle :title="header" />

      <div class="education__cards">
        <EducationCard
          title="Kemerovo State University"
          date="2011 - 2015"
          percentage="100"
          name="Computer Science and ICT (pedagogical education)"
          images="university"
        />
        <EducationCard />
        <EducationCard />
        <EducationCard />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.education {
  &__cards {
    display: flex;
    flex-wrap: wrap;
    gap: 4px;
    margin-top: 16px;
    margin-bottom: 24px;

    @media (max-width: 577px) {
      flex-direction: column;
    }
  }
}
</style>
