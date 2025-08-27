<template>
  <section>
    <h2>Skills</h2>
    <table id="skills-table">
      <thead>
        <tr>
          <th>Area</th>
          <th>Technologies</th>
        </tr>
      </thead>
      <tbody>
        <SkillAreaItem
          v-for="skillArea in skillAreas"
          :key="skillArea.area"
          :area="skillArea.area"
          :technologies="skillArea.technologies"
        />
      </tbody>
    </table>
  </section>
</template>

<script>
import SkillAreaItem from "../skills/SkillAreaItem.vue";

export default {
  name: "SkillsSection",
  components: {
    SkillAreaItem,
  },
  data() {
    return {
      skillAreas: [
        {
          area: "JavaScript",
          technologies: ["React.js", "Vue.js", "Node.js"],
        },
        {
          area: "Others",
          technologies: ["Git", "GitHub", "Azure DevOps", "CI/CD"],
        },
      ],
    };
  },
};
</script>
