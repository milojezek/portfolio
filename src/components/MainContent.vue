<template>
  <main>
    <h1>Frontend Development, JavaScript, TypeScript, ReactJS, VueJS</h1>
    <ProjectsSection />
    <section>
      <p
        class="about-text"
      >I’m Miloslav, a full stack developer based in Prague (Czechia) with over 3 years of experience in web development. I specialize in building web apps and websites. My go-to languages are JavaScript and TypeScript, but I'm always open to learning and using whatever is best for the job at hand. Lately, I've been diving into Go to expand my toolkit.</p>
    </section>
  </main>
</template>

<script>
import ProjectsSection from "./projects/ProjectsSection.vue";

export default {
  name: "MainContent",
  components: {
    ProjectsSection,
  },
};
</script>