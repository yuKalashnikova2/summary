<script>
import ContentTitle from './ContentTitle.vue'
import ToolsCard from './ToolsCard.vue'
export default {
  props: {
    header: String,
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

    <div class="section__cards">
      <ToolsCard
        name="Figma"
        image="figma"
        description="UI Design, prototyping "
      />
      <ToolsCard name="JavaSript" image="js" description="ES6" />
      <ToolsCard name="Vue" image="vue" description="JavaScript framework" />
      <ToolsCard name="VS Code" image="vs-code" description="Code Editor" />
      <ToolsCard name="Git" image="git" description="--fast-version-control" />
      <ToolsCard name="HTML5" image="html" description="Structural Design" />
      <ToolsCard name="CSS" image="css" description="Style Design" />
    </div>
  </div>
</template>
