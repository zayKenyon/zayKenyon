<script setup lang="ts">
import ProjectItem from './ProjectItem.vue';
import YamlContent from 'data/projects.yml';

const projects = YamlContent.projects;
</script>

<template>
  <h3>
    // Featured Projects and Experience:
    <br />
  </h3>

  <div v-for="project in projects" class="projects">
    <ProjectItem :project="project" />
  </div>
</template>
