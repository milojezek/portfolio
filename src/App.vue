<template>
  <header>
    <a href="/">Miloslav Jezek</a>
    <nav>
      <a href="#about">About</a>
    </nav>
  </header>
  <main>
    <h1>Web Development, JavaScript, TypeScript, ReactJS, VueJS, NodeJS</h1>
    <ProjectsSection />
    <section id="about">
      <p
        class="about-text"
      >I’m Miloslav, a full stack developer based in Prague (Czechia) with over 3 years of experience in web development. I specialize in building web apps and websites. My go-to languages are JavaScript and TypeScript, but I'm always open to learning and using whatever is best for the job at hand. Lately, I've been diving into Go to expand my toolkit.</p>
    </section>
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

