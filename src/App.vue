<template>
  <header>
    <a href="/">Miloslav Jezek</a>
    <nav>
      <a href="#about">About</a>
    </nav>
  </header>
  <main>
    <h1>Full-stack Development, JavaScript, TypeScript, NodeJS, ReactJS, VueJS</h1>
    <ProjectsSection />
    <section id="about">
      <p
        class="about-text"
      >I’m Miloslav Jezek, a full stack developer based in Prague (Czechia) with over 3 years of experience in building web applications and websites. My go-to programming languages are JavaScript and TypeScript, but I'm always open to learning and using whatever is best for the job at hand.</p>
    </section>
    <p class="about-text links">
      <a>LinkedIn</a>
    </p>
  </main>
  <footer>
    <p class="footer-text">© Miloslav Jezek 2025</p>
  </footer>
</template>

<script>
import ProjectsSection from "@components/projects/ProjectsSection.vue";

export default {
  name: "App",
  components: {
    ProjectsSection,
  },
};
</script>

