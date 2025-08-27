<template>
  <tr>
    <td>{{ area }}</td>
    <td>
      <span v-for="(tech, index) in technologies" :key="tech" class="tech-item">
        {{ tech }}
        <span v-if="index < technologies.length - 1" class="separator">|&nbsp;</span>
      </span>
    </td>
  </tr>
</template>

<script>
export default {
  name: "SkillAreaItem",
  props: {
    area: {
      type: String,
      required: true,
      default: "",
    },
    technologies: {
      type: Array,
      required: true,
      default: () => [],
    },
  },
};
</script>
