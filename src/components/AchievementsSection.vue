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
      <AchievementsCard
        subtitle="Hacktoberfest Contributor"
        title="Github"
        date="Oct 2023 - Nov 2023"
        decription="Contributed 8 PR’s in various open source projects. Great experience and learning alot about working with Github and open-source. Connecting with developers"
        logo="github"
      />
      <AchievementsCard
        subtitle="Contributor"
        title="Winter of Code"
        date="Oct 2023 - Nov 2023"
        decription="Overwhelming to be a part of DSC NSEC project - DSC NSEC Algorithms for Winter of Code 2020. First introduction to Git and Github. How github is used by most of the programmers in order to manage the projects."
        logo="5"
      />
      <AchievementsCard
        subtitle="30Days of Google Cloud"
        title="Google"
        date="Oct 2023 - Nov 2023"
        decription="Contributed 8 PR’s in various open source projects. Great experience and learning alot about working with Github and open-source. Connecting with developers"
        logo="google"
      />
    </div>
  </div>
</template>
