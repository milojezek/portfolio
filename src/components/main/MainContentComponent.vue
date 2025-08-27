<template>
  <main>
    <section>
      <div class="intro-header">
        <h1>Hey there! I'm Milo...</h1>
        <p>Full Stack Developer</p>
      </div>
      <h5 class="intro-description">
        Based in Prague (Czechia), but enjoyng the flexibility of working from anywhere.
        I love food, languages, travelling, playing volleyball, and building apps.
      </h5>
      <div class="links-container">
        <a href="/" target="_blank">Email me</a>
        <a href="https://www.linkedin.com/in/miloslav-jezek/" target="_blank">LinkedIn</a>
        <a href="https://github.com/milojezek" target="_blank">GitHub</a>
      </div>
      <div id="play-game">
        <button @click="toggleColorDiv">Wanna be creative?</button>
      </div>
      <div class="color-div" v-show="showColorDiv">
        <h4>Pick a color</h4>
        <p>Oops...</p>
        <input type="color" id="color-picker" value="#0084FF" />
        <button>Reset</button>
      </div>
    </section>
    <section>
      <h2>Skills</h2>
      <table>
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
  </main>
</template>

<script>
import SkillAreaItem from "@/components/SkillAreaItem.vue";

export default {
  name: "MainContentComponent",
  components: {
    SkillAreaItem,
  },
  data() {
    return {
      showColorDiv: false,
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
  methods: {
    toggleColorDiv() {
      this.showColorDiv = !this.showColorDiv;
    },
  },
};
</script>