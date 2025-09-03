<template>
  <section id="skills-section" class="skills-section">
    <h2>What I Do & Use</h2>
    <div class="skills-container">
      <SkillArea title="Web Development" :skills="webDevelopment" />
      <SkillArea title="Development Management" :skills="devManagement" />
    </div>
  </section>
</template>

<script>
import SkillAreaItem from "../skills/SkillAreaItem.vue";
import SkillArea from "../skills/SkillArea.vue";

export default {
  name: "SkillsSection",
  components: {
    SkillAreaItem,
    SkillArea,
  },
  data() {
    return {
      webDevelopment: [
        "JavaScript/TypeScript",
        "ReactJS",
        "VueJS",
        "HTML",
        "CSS",
        "NodeJS",
        "ExpressJS",
        "RESTful APIs",
        "PostgreSQL",
        "Go (learning)",
      ],
      devManagement: [
        "Git",
        "GitHub",
        "Azure DevOps",
        "Azure Resources",
        "Docker",
        "Iterative development",
        "Scrum",
        "Kanban",
      ],
    };
  },
};
</script>

<style scoped>
.skills-section {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.skills-container {
  background: var(--background-muted);
  border: 1px solid var(--border-primary);
  border-radius: var(--border-radius-large);
  padding: 1.5rem;
}
</style>