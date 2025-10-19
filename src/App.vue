<template>
  <header>
    <a href="https://milojezek.github.io/portfolio/">Miloslav Jezek</a>
    <nav>
      <a href="#about">About</a>
    </nav>
  </header>
  <main>
    <h1>Full-stack Developer</h1>
    <h1 style="color: #5a5a5a">JavaScript & TypeScript</h1>
    <h1 style="color: #5a5a5a">Node | Express | React | Vue</h1>
    <ProjectsSection />
    <section id="about" class="about-section">
      <div class="photo-links-container">
        <img src="@assets/mj_photo.png" alt="Miloslav Jezek Photo" class="photo" />
        <div class="social-links">
          <a href="https://www.linkedin.com/in/miloslav-jezek/" target="_blank" class="social-link">
            <img src="@/assets/linkedin_square_icon.png" alt="LinkedIn" class="social-icon" />
          </a>
          <a href="https://github.com/milojezek" target="_blank" class="social-link">
            <img src="@/assets/github_icon.png" alt="GitHub" class="social-icon" />
          </a>
        </div>
      </div>
      <div class="about-text-container">
        <p
          class="about-text"
        >I'm Miloslav Jezek, a developer based in Prague with experience building full-stack JavaScript/TypeScript web applications. JS & TS are my go-to languages, but I'm always happy to use whatever is most suitable for the job at hand. The backend is the area where I feel best and where I direct my efforts and growth.</p>
      </div>
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

