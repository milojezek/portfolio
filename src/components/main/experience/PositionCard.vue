<template>
  <div class="position-card">
    <details>
      <summary class="position-summary">
        <div class="position-header-main">
          <div class="company-logo">
            <img v-if="position.companyLogo" :src="position.companyLogo" :alt="position.company" />
            <div v-else class="logo-placeholder">{{ position.company.charAt(0) }}</div>
          </div>
          <div class="position-main-info">
            <h3 class="position-title">{{ position.title }}</h3>
            <div class="company-name">
              <div
                v-if="position.company && position.employmentType"
              >{{ position.company }} &middot; {{ position.employmentType }}</div>
              <div v-else-if="position.company">{{ position.company }}</div>
              <div v-else-if="position.employmentType">{{ position.employmentType }}</div>
            </div>
            <p class="position-duration">{{ position.duration }}</p>
            <p class="position-location">{{ position.location }}</p>
          </div>
        </div>
      </summary>

      <div class="position-content">
        <ul class="responsibilities-list" v-if="position.responsibilities.length > 0">
          <li
            v-for="responsibility in position.responsibilities"
            :key="responsibility"
          >{{ responsibility }}</li>
        </ul>

        <div v-if="position.skills.length > 0" class="skills-section">
          <div class="skills-label">Skills Used</div>
          <div class="skills-tags">
            <span class="skill-tag" v-for="skill in position.skills" :key="skill">{{ skill }}</span>
          </div>
        </div>
      </div>
    </details>

    <div v-if="showDivider" class="position-divider"></div>
  </div>
</template>

<script>
export default {
  name: "PositionCard",
  props: {
    position: {
      type: Object,
      required: true,
    },
    showDivider: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
.position-card {
  padding: 1.5rem 0;
  border-bottom: 1px solid var(--border-primary);
}

.position-card:last-child {
  border-bottom: none;
}

.position-header-main {
  display: flex;
  gap: 1rem;
  margin-bottom: 1rem;
}

.company-logo {
  flex-shrink: 0;
}

.company-logo img {
  width: 48px;
  height: 48px;
  border-radius: var(--border-radius-small);
  object-fit: cover;
}

.logo-placeholder {
  width: 48px;
  height: 48px;
  background: var(--color-link-transparent);
  color: var(--color-link);
  border-radius: var(--border-radius-small);
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 600;
  font-size: 1.25rem;
}

.position-main-info {
  flex: 1;
}

.position-title {
  font-size: 1.125rem;
  font-weight: 600;
  color: var(--color-primary);
  margin: 0 0 0.25rem 0;
}

.company-name {
  font-size: 0.875rem;
  color: var(--color-primary);
  margin: 0 0 0.25rem 0;
  font-weight: 500;
}

.position-duration,
.position-location {
  font-size: 0.875rem;
  color: #666;
  margin: 0;
  line-height: 1.4;
}

.position-content {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.responsibilities-list {
  margin: 0;
  padding-left: 1.5rem;
  color: var(--color-primary);
}

.responsibilities-list li {
  font-size: 0.875rem;
  line-height: 1.5;
  margin-bottom: 0.5rem;
}

.responsibilities-list li:last-child {
  margin-bottom: 0;
}

.skills-section {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

/* Details styling */
details {
  border-radius: var(--border-radius-small);
}

.position-summary {
  cursor: pointer;
  padding: 0.75rem;
  background: var(--background-muted);
  border: 1px solid var(--border-primary);
  border-radius: var(--border-radius-small);
  transition: all 0.2s ease;
  user-select: none;
  list-style: none;
  display: block;
  width: 100%;
}

.position-summary::-webkit-details-marker {
  display: none;
}

.position-summary::marker {
  display: none;
}

.position-summary:hover {
  background: var(--color-link-transparent);
  border-color: var(--color-link);
  transform: translateY(-1px);
}

.position-summary:hover .position-title {
  color: var(--color-link);
}

details[open] .position-summary {
  background: var(--color-link-transparent);
  border-color: var(--color-link);
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
  border-bottom: none;
}

details[open] .position-summary .position-title {
  color: var(--color-link);
}

details[open] {
  border: 1px solid var(--color-link);
  border-radius: var(--border-radius-small);
}

.position-header-main {
  display: flex;
  gap: 1rem;
  margin: 0;
}

details > *:not(summary) {
  padding: 0.75rem;
  border-top: 1px solid var(--border-primary);
  background: var(--background-primary);
  border-bottom-left-radius: var(--border-radius-small);
  border-bottom-right-radius: var(--border-radius-small);
}

.skills-label {
  font-size: 0.875rem;
  font-weight: 600;
  color: var(--color-primary);
}

.skills-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem;
}

.skill-tag {
  display: inline-block;
  padding: 0.2rem 0.6rem;
  background: var(--color-link-transparent);
  color: var(--color-link);
  border-radius: var(--border-radius-small);
  font-size: 0.75rem;
  line-height: 1.2;
}

.position-divider {
  width: 100%;
  height: 1px;
  background: var(--border-secondary);
  margin-top: 1rem;
  opacity: 0.5;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .position-card {
    padding: 1rem 0;
  }

  .responsibilities-list {
    padding-left: 1.2rem;
  }

  .responsibilities-list li {
    font-size: 0.8rem;
  }

  .skills-tags {
    gap: 0.3rem;
  }

  .skill-tag {
    font-size: 0.7rem;
    padding: 0.15rem 0.5rem;
  }

  .position-title {
    font-size: 1rem;
  }

  .company-name,
  .position-duration,
  .position-location {
    font-size: 0.8rem;
  }
}
</style>
