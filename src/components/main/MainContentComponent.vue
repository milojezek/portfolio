<template>
  <main>
    <section>
      <div class="intro-header">
        <h1>Hey there! I'm Milo...</h1>
        <p>Full Stack Developer</p>
      </div>
      <h5 class="intro-description">
        Based in Prague (Czechia), but enjoyng the flexibility of working from anywhere.
        I love food, languages, travelling, playing volleyball, and building apps.
      </h5>
      <div class="links-container">
        <a href="/" target="_blank">Email me</a>
        <a href="https://www.linkedin.com/in/miloslav-jezek/" target="_blank">LinkedIn</a>
        <a href="https://github.com/milojezek" target="_blank">GitHub</a>
      </div>
    </section>
    <SkillsSection />
    <ProjectsSection />
  </main>
</template>

<script>
import SkillsSection from "./skills/SkillsSection.vue";
import ProjectsSection from "./projects/ProjectsSection.vue";

export default {
  name: "MainContentComponent",
  components: {
    SkillsSection,
    ProjectsSection,
  },
};
</script>