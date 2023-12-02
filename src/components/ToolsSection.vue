<script>
import ContentTitle from './ContentTitle.vue'
import ToolsCard from './ToolsCard.vue'
export default {
  data() {
    return {
      isTools: true,
      isSkills: true,
    }
  },
  props: {
    header: {
        type: String,
        required: true
    },
  },
  components: {
    ToolsCard,
    ContentTitle,
  },
}
</script>

<template>
  <div class="section">
    <ContentTitle :title="header" />

    <div
      class="section__cards section__cards_margin-bottom-0"
    >
      <ToolsCard
        name="Figma"
        image="figma"
        description="UI Design, prototyping "
        isTools
      />
      <ToolsCard name="JavaSript" image="js" description="ES6" isTools />
      <ToolsCard
        name="Vue"
        image="vue"
        description="JavaScript framework"
        isTools
      />
    </div>
    <div class="section__cards section__cards_margin-top-small">
      <ToolsCard
        name="VS Code"
        image="vs-code"
        description="Code Editor"
        isSkills
      />
      <ToolsCard
        name="Git"
        image="git"
        description="--fast-version-control"
        isSkills
      />
      <ToolsCard
        name="HTML5"
        image="html"
        description="Structural Design"
        isSkills
      />
      <ToolsCard name="CSS" image="css" description="Style Design" isSkills />
      <ToolsCard name="CSS" image="css" description="Style Design" isSkills />
      <ToolsCard name="CSS" image="css" description="Style Design" isSkills />
    </div>
  </div>
</template>
