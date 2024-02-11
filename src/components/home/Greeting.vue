<script setup lang="ts">
import YamlContent from 'data/config.yml'

const greeting = YamlContent.meta.header
const missionStatement = YamlContent.meta.description
</script>

<template>
  <h1>{{ greeting }}</h1>
  {{ missionStatement }}
</template>
