<script setup lang="ts">
import YamlContent from 'data/config.yml';

const interestItems = YamlContent.meta.facts[2].items;
</script>

<template>
  <h3>// What I'm interested in:</h3>
  <ul v-for="item in interestItems" class="no-bullets">
    <li>
      {{ item.title }}
    </li>
  </ul>
</template>
