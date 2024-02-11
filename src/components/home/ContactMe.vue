<script setup lang="ts">
import YamlContent from 'data/config.yml'

const contactDetails = YamlContent.contact
</script>

<template>
  <h3>Get in touch:</h3>
  <a :href="'mailto:' + contactDetails.email">{{ contactDetails.email }}</a>
  <ul v-for="link in contactDetails.links">
    <li>
      <a :href="link.url" target="_blank"> {{ link.title }} - {{ link.username }} </a>
    </li>
  </ul>
</template>
