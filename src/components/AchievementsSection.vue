<script>
import ContentTitle from './ContentTitle.vue'
import AchievementsCard from './AchievementsCard.vue'
export default {
  props: {
    header: String,
  },
  components: {
    AchievementsCard,
    ContentTitle,
  },
}
</script>

<template>
  <div class="section">
    <ContentTitle :title="header" />

    <div class="section__cards">
      <AchievementsCard />
    </div>
  </div>
</template>
