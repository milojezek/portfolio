<template>
  <section>
    <div class="intro-row">
      <div class="intro-photo">
        <img src="@/assets/images/intro_photo.png" alt="Milo's photo" />
      </div>
      <div class="intro-content">
        <div class="intro-header">
          <h1>Hey there! I'm Milo...</h1>
          <p>Full Stack Developer</p>
        </div>
        <h5 class="intro-description">
          Based in Prague (Czechia), but enjoyng the flexibility of working from anywhere.
          I love food, languages, travelling, playing volleyball, and building apps.
        </h5>
        <div class="links-container">
          <a href="https://www.linkedin.com/in/miloslav-jezek/" target="_blank" class="icon-link">
            <img src="@assets/icons/linkedin-icon.png" alt="LinkedIn" class="icon-img" />
          </a>
          <a href="https://github.com/milojezek" target="_blank" class="icon-link">
            <img src="@assets/icons/github-icon.png" alt="GitHub" class="icon-img" />
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "IntroSection",
};
</script>

<style scoped>
.intro-row {
  display: flex;
  align-items: center;
  gap: 2rem;
}

.intro-photo {
  max-width: 30%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.intro-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.intro-header p {
  padding-top: 0.25rem;
}

.intro-description {
  max-width: 500px;
}

.links-container {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem 0;
}

.icon-link {
  display: flex;
  align-items: center;
}

.icon-img {
  width: 50px;
  height: 50px;
  object-fit: contain;
}

@media (max-width: 640px) {
  .intro-row {
    flex-direction: column;
    align-items: stretch;
    gap: 1.5rem;
  }
  .intro-photo {
    order: 2;
    max-width: 100%;
    margin-top: 1rem;
  }
  .intro-content {
    order: 1;
    display: flex;
    flex-direction: column;
  }
  .links-container {
    justify-content: center;
    margin-top: 1rem;
    padding: 0.5rem 0;
  }
}
</style>
