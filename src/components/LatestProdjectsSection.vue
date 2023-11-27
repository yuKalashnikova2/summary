<script>
import ContentTitle from './ContentTitle.vue'
import LatestProjectsCard from './LatestProjectsCard.vue'

export default {
  props: {
    header: {
      type: String,
      required: true,
    },
  },
  components: {
    ContentTitle,
    LatestProjectsCard,
  },
}
</script>

<template>
  <div class="section">
    <ContentTitle :title="header" />

    <div class="section__cards section__cards_gap-medium">
      <LatestProjectsCard
        title="Portfolio Webpage"
        description="Personal Portfolio webpage with resume and blog"
        image="sm"
        link="https://github.com/yuKalashnikova2"
      />
      <LatestProjectsCard
        title="Everything"
        description="For exemple"
        image="js"
        link="Here is link"
      />
    </div>
  </div>
</template>
