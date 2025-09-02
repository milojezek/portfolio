<template>
  <div class="skill-area">
    <div class="skill-area-title">
      <h3>{{ title }}</h3>
    </div>
    <div class="skill-tags-grid">
      <div class="card-button-secondary" v-for="skill in skills" :key="skill">
        <p>{{ skill }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SkillArea",
  props: {
    title: {
      type: String,
      required: true,
    },
    skills: {
      type: Array,
      required: true,
      default: () => [],
    },
  },
};
</script>

<style scoped>
.skill-area {
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
  padding: 1rem;
  border-bottom: 1px solid var(--border-primary);
  position: relative;
}

.skill-area:last-child {
  border-bottom: none;
}

.skill-area-title {
  align-self: flex-start;
}

.skill-area-title h3 {
  font-size: 1rem;
  font-weight: 600;
  color: var(--color-primary);
  margin: 0;
}

.skill-tags-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  width: 100%;
}

.skill-tags-grid .card-button-secondary {
  padding: 0.25rem 0.75rem;
  border-radius: var(--border-radius-small);
  font-size: 0.875rem;
}

.skill-tags-grid p {
  margin: 0;
  font-size: 0.875rem;
  line-height: 1.2;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .skill-area {
    padding: 1rem;
    gap: 0.5rem;
  }
}
</style>