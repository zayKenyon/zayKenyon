<script setup lang="ts">
import YamlContent from 'data/config.yml';

const contactDetails = YamlContent.contact;
</script>

<template>
  <h3>
    // Get in touch:
    <br />
    <a :href="'mailto:' + contactDetails.email">{{ contactDetails.email }}</a>
  </h3>

  <div class="social-links">
    <ul v-for="link in contactDetails.links" class="no-bullets">
      <li>
        <a :href="link.url" target="_blank"
          >knyn.uk/{{ link.title.toLowerCase() }}
          <br />
          <i>@{{ link.username }}</i>
        </a>
      </li>
    </ul>
  </div>
</template>
<style scoped>
.social-links {
  display: flex;
  justify-content: flex-start;
  gap: 1rem;
}
</style>
