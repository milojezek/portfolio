<template>
  <HeaderComponent />
  <MainContentComponent />
  <FooterComponent />
</template>

<script>
import HeaderComponent from "@/components/header/HeaderComponent.vue";
import FooterComponent from "@/components/footer/FooterComponent.vue";
import MainContentComponent from "@/components/main/MainContentComponent.vue";

export default {
  name: "App",
  components: {
    HeaderComponent,
    MainContentComponent,
    FooterComponent,
  },
};
</script>

