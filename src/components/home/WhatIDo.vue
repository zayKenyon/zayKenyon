<script setup lang="ts">
import YamlContent from 'data/config.yml';

const whatIDoItems = YamlContent.meta.facts[1].items;
</script>

<template>
  <h3>// What I do:</h3>
  <ul v-for="item in whatIDoItems" class="no-bullets">
    <li>
      <a :href="item.link" target="_blank">
        {{ item.title }}
      </a>
    </li>
  </ul>
</template>
