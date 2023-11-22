<script>
import ContentTitle from './ContentTitle.vue'
import EducationCard from './EducationCard.vue'
export default {
  components: {
    ContentTitle,
    EducationCard,
  },
  props: {
    header: String,
  },
  // data() {
  //   return {
  //     headersMainBlock: [
  //       {
  //         id: 1,
  //         title: 'Education'
  //       },
  //       {
  //         id: 2,
  //         title: 'Achievements'
  //       },
  //       {
  //         id: 3,
  //         title: 'Tools/Skills'
  //       },   {
  //         id: 4,
  //         title: 'Latest projects'
  //       },
  //       {
  //         id: 5,
  //         title: 'Certificates & Awards'
  //       }
  //     ],
  //   }
  // },
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
