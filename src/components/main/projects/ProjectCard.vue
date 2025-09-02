<template>
  <div class="project-card">
    <div>
      <p>{{ date }}</p>
      <h4>{{ title }}</h4>
      <div class="skill-list">
        <div class="card-button-secondary" v-for="tech in technologies" :key="tech">
          <p>{{ tech }}</p>
        </div>
      </div>
      <p>{{ description }}</p>
      <div class="project-links">
        <a :href="liveUrl" target="_blank" v-if="liveUrl">Live</a>
        <a :href="githubUrl" target="_blank" v-if="githubUrl">GitHub</a>
      </div>
    </div>
    <div class="img-div" v-if="image">
      <img class="big-img" :src="image" :alt="title" />
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectCard",
  props: {
    date: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    technologies: {
      type: Array,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    liveUrl: {
      type: String,
      default: null,
    },
    githubUrl: {
      type: String,
      default: null,
    },
    image: {
      type: String,
      default: null,
    },
  },
};
</script>

<style scoped>
.project-card {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  border: 1px solid darkgray;
  box-shadow: 10px 10px;
  border-radius: 0.75rem;
  padding: 1.5rem;
}

.project-card:hover {
  box-shadow: 10px 10px var(--color-green-highlight);
}

.project-card > div:first-of-type {
  flex: 1;
}

.project-links {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding-top: 0.5rem;
}

@media (min-width: 640px) {
  .project-card {
    flex-direction: row;
    align-items: center;
  }

  .project-card .img-div {
    max-width: 30%;
  }
}
</style>
