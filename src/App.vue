<template>
  <div id="app">
    <header class="fade-in">
      <a href="https://milojezek.github.io/portfolio/">Miloslav Jezek</a>
      <nav>
        <a href="#about">About</a>
      </nav>
    </header>
    <main>
      <h1 class="fade-in fade-in-delay-1">Full-stack Developer</h1>
      <h1 class="fade-in fade-in-delay-2" style="color: #5a5a5a">JavaScript & TypeScript</h1>
      <h1 class="fade-in fade-in-delay-3" style="color: #5a5a5a">Node | Express | React | Vue</h1>
      <div class="fade-in fade-in-delay-4">
        <ProjectsSection />
      </div>
      <section id="about" class="about-section fade-in">
        <div class="photo-links-container">
          <img src="@assets/mj_photo.png" alt="Miloslav Jezek Photo" class="photo" />
          <div class="social-links">
            <a
              href="https://www.linkedin.com/in/miloslav-jezek/"
              target="_blank"
              class="social-link"
            >
              <img src="@/assets/linkedin_square_icon.png" alt="LinkedIn" class="social-icon" />
            </a>
            <a href="https://github.com/milojezek" target="_blank" class="social-link">
              <img src="@/assets/github_icon.png" alt="GitHub" class="social-icon" />
            </a>
            <a href="mailto:milekdeveloper@gmail.com" class="social-link">
              <img src="@/assets/email_square_icon.png" alt="E-mail" class="social-icon" />
            </a>
          </div>
        </div>
        <div class="about-text-container">
          <p
            class="about-text"
          >I'm Miloslav Jezek, a developer based in Prague with experience building full-stack TypeScript web applications. JS & TS are my go-to languages, but I'm always happy to use whatever is most suitable for the job at hand. The backend is the area where I feel best and where I direct my efforts and growth, but I also enjoy building clean, easy-to-navigate user interfaces.</p>
          <p
            class="about-text"
            style="margin-top: 1.5rem;"
          >This portfolio is my small digital space where I'll showcase my recent personal work. I'm particularly interested in projects related to languages, travelling, health, and anything that makes living easier. Whether it's a complete app or a small utility tool.</p>
        </div>
      </section>
    </main>
    <footer class="fade-in">
      <p class="footer-text">© Miloslav Jezek 2025</p>
    </footer>
  </div>
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

