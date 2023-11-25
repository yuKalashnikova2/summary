<script>
import ContentTitle from './ContentTitle.vue'
import SertificateCard from './SertificateCard.vue'

export default {
  props: {
    header: String,
  },
  components: {
    ContentTitle,
    SertificateCard,
  },
}
</script>

<template>
  <div class="section">
    <ContentTitle :title="header" />

    <div class="section__cards section__cards_gap-medium">
      <SertificateCard
        title="Coursera"
        subtitle="Frontend Everyday (Vue 3 + Pinia)"
        date="Nov 2023 - April 2024"
        image="vue"
        location="Online"
      />
      <SertificateCard
        title="Coursera"
        subtitle="Frontend Everyday (Vue 3 + Pinia)"
        date="Nov 2023 - April 2024"
        image="vue"
        location="Online"
      />
    </div>
  </div>
</template>
