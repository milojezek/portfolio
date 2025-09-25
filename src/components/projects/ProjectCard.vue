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


