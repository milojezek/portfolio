<template>
  <main>
    <IntroSection />
    <SkillsSection />
    <ProjectsSection />
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

<style scoped>
/* intro-header styles moved to IntroHeader.vue */

/* intro section styles moved to IntroSection.vue */
</style>