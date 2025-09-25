<template>
  <header>
    <a href="/">Miloslav Jezek</a>
    <nav>
      <a href="/">About</a>
    </nav>
  </header>
  <MainContent />
  <footer>
    <p class="footer-text">© Miloslav Jezek 2025</p>
  </footer>
</template>

<script>
import MainContent from "@/components/MainContent.vue";

export default {
  name: "App",
  components: {
    MainContent,
  },
};
</script>

