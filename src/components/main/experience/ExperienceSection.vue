<template>
  <section id="experience-section" class="experience-section">
    <h2>Work Experience</h2>
    <div class="experience-container">
      <PositionCard
        v-for="position in positions"
        :key="position.id"
        :position="position"
        :show-divider="position.id !== positions[positions.length - 1].id"
      />
    </div>
  </section>
</template>

<script>
import PositionCard from "./PositionCard.vue";
import hrIcon from "@/assets/icons/work_hr.png";
import itIcon from "@/assets/icons/work_it.png";

export default {
  name: "ExperienceSection",
  components: {
    PositionCard,
  },
  data() {
    return {
      positions: [
        {
          id: 1,
          title: "Full Stack Developer",
          company: "FPT Czech",
          companyLogo: itIcon,
          duration: "Jul 2025 - Present",
          location: "Prague Metropolitan Area · Hybrid",
          employmentType: "Full-time",
          responsibilities: [
            "Working on multiple projects as a full-stack and frontend developer, keeping various codebases organized and communicating with different stakeholders",
            "Building UI for a data-heavy web app for a client with extensive form handling and data manipulation using TypeScript and React",
            "Migrating company websites from traditional WordPress to a headless architecture with Vue.js, improving their security and adding dynamic features",
            "Maintaining and troubleshooting an internal data management platform I built, fixing bugs and providing developer support to keep everything running smoothly",
          ],
          skills: [
            "TypeScript",
            "Vue.js",
            "React.js",
            "Azure DevOps",
            "Azure",
            "HTML",
            "Cascading Style Sheets (CSS)",
            "Node.js",
            "WordPress",
            "JavaScript",
            "PostgreSQL",
          ],
        },
        {
          id: 2,
          title: "Product Developer",
          company: "FPT Czech",
          companyLogo: itIcon,
          duration: "Jun 2024 - Jul 2025",
          location: "Prague Metropolitan Area · Hybrid",
          employmentType: "Full-time",
          responsibilities: [
            "Built a data management platform from scratch that replaced hours of communication and manual tasks with user-friendly features and a single source of internal employee data",
            "Wore two hats as both product owner and one of the main developers",
            "Developed core features while making sure everything solved real business problems",
            "Started and led the initiative - assembled the team, set the direction, and kept everyone aligned",
            "Occasionally helped with company website development",
          ],
          skills: [
            "Azure DevOps",
            "Node.js",
            "styled-components",
            "User Experience (UX)",
            "Product Development",
            "User Stories",
            "Backlog Management",
            "JavaScript",
            "Communication",
            "TypeScript",
            "Sequelize.js",
            "Vue.js",
            "Scrum",
            "React.js",
            "Express.js",
            "Web Application Development",
            "Web Development",
            "PostgreSQL",
            "Web Design",
            "Software Development",
            "Product Design",
            "Team Management",
          ],
        },
        {
          id: 3,
          title: "Javascript Developer",
          company: "FPT Czech",
          companyLogo: itIcon,
          duration: "Jun 2023 - May 2024",
          location: "Prague Metropolitan Area · Hybrid",
          employmentType: "Full-time",
          responsibilities: [
            "Converted an incomplete employee app written in React Native into a progressive web app (PWA)",
            "Helped with tooling and operational tasks alongside development work",
          ],
          skills: [
            "React Native",
            "Azure DevOps",
            "Azure",
            "HTML",
            "styled-components",
            "Teamwork",
            "Cascading Style Sheets (CSS)",
            "Progressive Web Applications (PWAs)",
            "JavaScript",
            "Communication",
            "Git",
            "Scrum",
            "React.js",
            "Web Application Development",
            "Web Development",
            "Software Development",
            "HTML5",
          ],
        },
        {
          id: 4,
          title: "Java Developer",
          company: "FPT Czech",
          companyLogo: itIcon,
          duration: "Feb 2023 - May 2023",
          location: "Prague Metropolitan Area · Hybrid",
          employmentType: "Full-time",
          responsibilities: [
            "Started as a Java developer working on a backend system",
            "Transitioned into web development with JS/TS due to limited Java projects",
          ],
          skills: [
            "HTML",
            "Thymeleaf",
            "Spring Boot",
            "Cascading Style Sheets (CSS)",
            "JavaScript",
            "Java",
            "PostgreSQL",
          ],
        },
        {
          id: 5,
          title: "Career transition",
          company: "",
          companyLogo: itIcon,
          duration: "Mar 2022 - Jan 2023",
          location: "Prague Metropolitan Area",
          employmentType: "",
          isCareerBreak: true,
          responsibilities: [
            "Took a few months off to fully focus on transitioning from HR to software development",
          ],
          skills: [],
        },
        {
          id: 6,
          title: "Technical Sourcer",
          company: "Wrike",
          companyLogo: hrIcon,
          duration: "May 2021 - Feb 2022",
          location: "Prague, Czechia · Hybrid",
          employmentType: "Full-time",
          responsibilities: [
            "Sourced potential candidates across the EU, UK, and Russia",
            "Used Python to automate repetitive tasks and improve efficiency",
          ],
          skills: [
            "IT Recruitment",
            "Teamwork",
            "Communication",
            "Sourcing",
            "Screening Resumes",
            "Python",
          ],
        },
        {
          id: 7,
          title: "IT Talent Sourcer",
          company: "GoodCall",
          companyLogo: hrIcon,
          duration: "Sep 2019 - Apr 2021",
          location: "Prague, Czechia · Hybrid",
          employmentType: "Full-time",
          responsibilities: [
            "Identified candidates for multiple client companies",
            "Conducted interviews both online and in person",
            "Streamlined recruitment workflows through automation",
          ],
          skills: [
            "IT Recruitment",
            "Teamwork",
            "Communication",
            "Sourcing",
            "Screening Resumes",
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
.experience-section {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.experience-container {
  background: var(--background-muted);
  border: 1px solid var(--border-primary);
  border-radius: var(--border-radius-large);
  padding: 1.5rem;
}
</style>
