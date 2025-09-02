<template>
  <section id="skills-section" class="skills-section">
    <h2>Skills</h2>
    <div class="skills-container">
      <SkillArea title="Frontend" :skills="frontend" />
      <SkillArea title="Backend" :skills="backend" />
      <SkillArea title="DevOps" :skills="devops" />
      <SkillArea title="Work Management" :skills="workManagement" />
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
      frontend: [
        "JavaScript/TypeScript",
        "ReactJS",
        "VueJS",
        "HTML",
        "CSS",
        "styled-components",
        "TailwindCSS",
        "Responsive Design",
        "UI/UX principles",
      ],
      backend: [
        "JavaScript/TypeScript",
        "NodeJS",
        "ExpressJS",
        "RESTful APIs",
        "PostgreSQL",
      ],
      devops: ["Git", "GitHub", "Azure DevOps", "Azure Resources"],
      workManagement: ["Iterative development", "Scrum", "Kanban"],
    };
  },
};
</script>

<style scoped>
.skills-section {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.skills-container {
  background: var(--background-muted);
  border: 1px solid var(--border-primary);
  border-radius: var(--border-radius-large);
  padding: 1.5rem;
}
</style>