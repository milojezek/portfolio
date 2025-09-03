<template>
  <div class="project-card" :style="{ backgroundImage: `url(${image})` }">
    <div class="project-overlay">
      <div class="project-content">
        <h4>{{ title }}</h4>
        <p class="project-description">{{ description }}</p>
        <a v-if="projectUrl" :href="projectUrl" target="_blank" class="visit-button">Visit Website →</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectCard",
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    projectUrl: {
      type: String,
      default: null,
    },
    image: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.project-card {
  position: relative;
  height: 300px;
  border-radius: 1rem;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  overflow: hidden;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.project-card:hover {
  transform: translateY(-5px);
}

.project-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.1);
  opacity: 0;
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2rem;
}

.project-card:hover .project-overlay {
  opacity: 1;
  background: rgba(0, 0, 0, 0.7);
}

.project-content {
  text-align: center;
  color: white;
  max-width: 100%;
}

.project-content h4 {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 1rem;
  color: white;
}

.project-description {
  font-size: 0.9rem;
  line-height: 1.4;
  margin-bottom: 1.5rem;
  opacity: 0.9;
}

.visit-button {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  background: transparent;
  color: white;
  border: 2px solid white;
  border-radius: 2rem;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.3s ease;
}

.visit-button:hover {
  background: white;
  color: #000;
  transform: translateY(-2px);
}

@media (min-width: 640px) {
  .project-card {
    height: 350px;
  }

  .project-content h4 {
    font-size: 1.75rem;
  }

  .project-description {
    font-size: 1rem;
  }
}
</style>
