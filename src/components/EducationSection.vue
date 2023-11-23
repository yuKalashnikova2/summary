<script>
import ContentTitle from './ContentTitle.vue'
import EducationCard from './EducationCard.vue'
export default {
  props: {
    header: String,
  },
  components: {
    EducationCard,
    ContentTitle,
  },
}
</script>

<template>
  <div class="section">
    <ContentTitle :title="header" />

    <div class="section__cards">
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
</template>
