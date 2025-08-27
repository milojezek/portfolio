<template>
  <section>
    <h2>Latest Projects</h2>
    <div class="cards-grid">
      <ProjectCard
        v-for="project in projects"
        :key="project.id"
        :date="project.date"
        :title="project.title"
        :technologies="project.technologies"
        :description="project.description"
        :live-url="project.liveUrl"
        :github-url="project.githubUrl"
        :image="project.image"
      />
    </div>
  </section>
</template>

<script>
import ProjectCard from "./ProjectCard.vue";
import bearImage from "@/assets/images/bear.jpg";

export default {
  name: "ProjectsSection",
  components: {
    ProjectCard,
  },
  data() {
    return {
      projects: [
        {
          id: 1,
          date: "August 27, 2025",
          title: "My Portfolio",
          technologies: ["VueJS", "Vite", "CSS"],
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
          liveUrl: "/",
          githubUrl: "/",
          image: bearImage,
        },
        {
          id: 2,
          date: "August 27, 2025",
          title: "My Portfolio",
          technologies: ["VueJS", "Vite", "CSS"],
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
          liveUrl: "/",
          githubUrl: "/",
          image: bearImage,
        },
      ],
    };
  },
};
</script>
