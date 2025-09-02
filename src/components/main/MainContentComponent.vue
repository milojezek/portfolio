<template>
  <main>
    <IntroSection />
    <SkillsSection />
    <ProjectsSection />
    <ExperienceSection />
  </main>
</template>

<script>
import SkillsSection from "./skills/SkillsSection.vue";
import ExperienceSection from "./experience/ExperienceSection.vue";
import ProjectsSection from "./projects/ProjectsSection.vue";
import IntroSection from "./intro/IntroSection.vue";

export default {
  name: "MainContentComponent",
  components: {
    IntroSection,
    SkillsSection,
    ExperienceSection,
    ProjectsSection,
  },
};
</script>