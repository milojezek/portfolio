<template>
  <section id="projects-section">
    <h2 class="fade-in">Recent Work</h2>
    <p
      class="fade-in placeholder-note"
    >This section currently shows random texts and images - real projects will be added later.</p>
    <div class="cards-grid">
      <div
        v-for="(project) in projects"
        :key="project.id"
        class="fade-in"
        :class="'fade-in-delay-2'"
      >
        <ProjectCard
          :title="project.title"
          :description="project.description"
          :projectUrl="project.projectUrl"
          :image="project.image"
        />
      </div>
    </div>
  </section>
</template>

<script>
import ProjectCard from "./ProjectCard.vue";

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
          title: "Random Project",
          description: "One random project randomly written by me.",
          projectUrl: "https://example.com",
          image:
            "https://images.unsplash.com/photo-1560518883-ce09059eeffa?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80",
        },
        {
          id: 2,
          title: "Randomisten",
          description: "Another random project randomly put here.",
          projectUrl: "https://example.com",
          image:
            "https://images.unsplash.com/photo-1554224155-6726b3ff858f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80",
        },
        {
          id: 3,
          title: "Three Is Magic",
          description: "Three is a magical number. Ideal for ideality.",
          projectUrl: "https://example.com",
          image:
            "https://images.unsplash.com/photo-1451187580459-43490279c0fa?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80",
        },
        {
          id: 4,
          title: "Not the End",
          description:
            "This project card is the last one but it's definitely not the end.",
          projectUrl: "https://example.com",
          image:
            "https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80",
        },
      ],
    };
  },
};
</script>


