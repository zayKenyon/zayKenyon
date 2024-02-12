<script setup lang="ts">
import Projects from '@/components/home/Projects.vue';

interface Project {
  title: string;
  role: string;
  web: boolean;
  tags: [string];
  dates: {
    start: string;
    end: string;
  };
  headline: string;
  links: [string];
  image: {
    file: string;
    position: string;
  };
  desc: string;
}

defineProps<{
  project: Project;
}>();
</script>

<template>
  <details>
    <summary class="project-info">
      <div class="project-meta">
        <p class="project-role">{{ project.role }}</p>
        <p class="project-title">{{ project.title }}</p>

        <div class="project-dates">
          <p>
            {{ project.dates.start }} -
            {{ project.dates.end === '~' ? 'Present' : project.dates.end }}
          </p>
        </div>

        <div class="project-"></div>
      </div>
    </summary>
  </details>
</template>
<style scoped>
.project-info {
  display: flex;
  flex-direction: row;
  border-radius: 0.25em;
  cursor: pointer;
  margin: -1em;
  padding: 1em 1em 0;
  transition: background-color 0.2s linear;

  &:hover,
  &:focus {
    background: var(--white);
  }

  @media only screen and (max-width: 768px) {
    flex-direction: column;
  }
}

.project-meta {
  flex: 1 1 auto;
  margin: 0 0.5em 0 0;

  @media only screen and (max-width: 768px) {
    margin: 0;
  }
}
.project-role {
  font-size: 1.15rem;
  margin: 0.5em 0;
}

.project-title {
  font-size: 1.15rem;
  margin: 0.5em 0;
}

.project-dates {
  display: flex;
  flex-flow: row wrap;

  .project-end {
    &.active {
      font-style: italic;
    }
  }
}

.project-tags {
  display: flex;
  flex: 0 1 auto;
  flex-flow: row wrap;
  margin: 0.5em 0;

  .project-tag {
    background: rgba(255, 255, 255, 0.25);
    border-radius: 0.25em;
    margin: 0.5em;
    padding: 0.5em 1em;
  }
}
</style>
