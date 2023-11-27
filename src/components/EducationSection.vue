<script>
import ContentTitle from './ContentTitle.vue'
import EducationCard from './EducationCard.vue'
export default {
  props: {
    header: {
      type: String,
      required: true,
    },
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
        :percentage="100"
        name="Computer Science and ICT (pedagogical education)"
        images="university"
      />
      <EducationCard
        title="Retraining courses"
        date="Aug 2016 - Nov 2016"
        :percentage="100"
        name="Russian language and literature (pedagogical education)"
        images="university"
      />
    </div>
  </div>
</template>
