<template>
  <main>
    <IntroSection />
  </main>
</template>

<script>
import SkillsSection from "./skills/SkillsSection.vue";
import ProjectsSection from "./projects/ProjectsSection.vue";
import IntroSection from "./intro/IntroSection.vue";

export default {
  name: "MainContentComponent",
  components: {
    IntroSection,
    SkillsSection,
    ProjectsSection,
  },
};
</script>