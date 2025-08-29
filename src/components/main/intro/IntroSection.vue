<template>
  <section>
    <div class="intro-row">
      <div class="intro-photo">
        <img :src="introPhoto" alt="Milo's photo" />
      </div>
      <div class="intro-content">
        <div class="intro-header">
          <h1>{{ headingText }}</h1>
          <div class="intro-divider"></div>
        </div>
        <h5 class="intro-description">{{ descriptionText }}</h5>
        <div class="links-container">
          <a :href="linkedinUrl" target="_blank" class="icon-link">
            <img :src="linkedinIcon" alt="LinkedIn" class="icon-img" />
          </a>
          <a :href="githubUrl" target="_blank" class="icon-link">
            <img :src="githubIcon" alt="GitHub" class="icon-img" />
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import linkedinIcon from "@/assets/icons/linkedin_icon.png";
import githubIcon from "@/assets/icons/github_icon.png";
import introPhoto from "@/assets/images/intro_photo_no_bg.png";

export default {
  name: "IntroSection",
  data() {
    return {
      headingText: "Hey there! I'm Milo...",
      descriptionText:
        "A Prague-based full-stack developer enjoying the flexibility of working from anywhere. I love food, languages, traveling, playing volleyball, and building apps.",
      linkedinUrl: "https://www.linkedin.com/in/miloslav-jezek/",
      githubUrl: "https://github.com/milojezek",
      linkedinIcon,
      githubIcon,
      introPhoto,
    };
  },
};
</script>

<style scoped>
.intro-row {
  display: flex;
  align-items: center;
  gap: 2rem;
}

.waving-hand {
  display: inline-flex;
  align-items: center;
  height: 1em;
  vertical-align: middle;
  margin-right: 0.4em;
}

.waving-hand-img {
  height: 1em;
  width: 1em;
  object-fit: contain;
}

.intro-divider {
  width: 100%;
  height: 2px;
  background: #00a825;
  border-radius: 2px;
  margin: 1rem 0 0.5rem 0;
}

.intro-photo {
  max-width: 35%;
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
    align-items: center;
    gap: 1.5rem;
  }
  .intro-photo {
    order: 2;
    max-width: 75%;
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
