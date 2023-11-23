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
    <slot :header="header"></slot>
  </div>
</template>

<style lang="scss">

</style>
