<template>
  <div class="company-experience">
    <div class="company-header">
      <div class="company-logo">
        <img v-if="company.logo" :src="company.logo" :alt="company.name" />
        <div v-else class="logo-placeholder">{{ company.name.charAt(0) }}</div>
      </div>
      <div class="company-info">
        <h3 class="company-name">{{ company.name }}</h3>
        <p class="company-details">{{ company.employmentType }} · {{ company.duration }}</p>
        <p class="company-location">{{ company.location }}</p>
      </div>
    </div>

    <div class="positions-list">
      <PositionCard
        v-for="position in company.positions"
        :key="position.id"
        :position="position"
        :is-career-break="company.isCareerBreak"
        :show-divider="company.positions.length > 1 && position.id !== company.positions[company.positions.length - 1].id"
      />
    </div>
  </div>
</template>

<script>
import PositionCard from "./PositionCard.vue";

export default {
  name: "CompanyExperience",
  components: {
    PositionCard,
  },
  props: {
    company: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.company-experience {
  padding: 1.5rem 0;
  border-bottom: 1px solid var(--border-primary);
}

.company-experience:last-child {
  border-bottom: none;
}

.company-header {
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

.company-info {
  flex: 1;
}

.company-name {
  font-size: 1.125rem;
  font-weight: 600;
  color: var(--color-primary);
  margin: 0 0 0.25rem 0;
}

.company-details,
.company-location {
  font-size: 0.875rem;
  color: #666;
  margin: 0;
  line-height: 1.4;
}

.positions-list {
  margin-left: 3rem;
}

@media (max-width: 768px) {
  .company-experience {
    padding: 1rem 0;
  }

  .positions-list {
    margin-left: 0;
    margin-top: 1rem;
  }
}
</style>
