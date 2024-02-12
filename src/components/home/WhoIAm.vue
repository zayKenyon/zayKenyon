<script setup lang="ts">
import YamlContent from 'data/config.yml';

const whoIAmItems = YamlContent.meta.facts[0].items;
</script>

<template>
  <h3>// Who I am:</h3>
  <ul v-for="item in whoIAmItems" class="no-bullets">
    <li>
      {{ item.title }}
    </li>
  </ul>
</template>
