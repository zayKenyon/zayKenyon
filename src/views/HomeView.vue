<script setup lang="ts">
import Greeting from '../components/home/Greeting.vue';
import WhoIAm from '../components/home/WhoIAm.vue';
import WhatIDo from '../components/home/WhatIDo.vue';
import WhatImInterestedIn from '../components/home/WhatImInterestedIn.vue';
import Projects from '../components/home/Projects.vue';
import ContactMe from '../components/home/ContactMe.vue';
import YamlContent from 'data/config.yml';

const showWhoIAm = YamlContent.meta.facts[0].web as boolean;
const showWhatIDo = YamlContent.meta.facts[1].web as boolean;
const showWhatImInterestedIn = YamlContent.meta.facts[2].web as boolean;
</script>

<template>
  <main>
    <div><Greeting /></div>
    <div class="profile-facts">
      <div v-if="showWhatIDo"><WhatIDo /></div>
      <div v-if="showWhoIAm"><WhoIAm /></div>
      <div v-if="showWhatImInterestedIn"><WhatImInterestedIn /></div>
    </div>
    <div class="projects">
      <Projects />
    </div>
    <ContactMe />
  </main>
</template>

<style scoped>
.profile-facts {
  display: flex;
  flex-wrap: wrap;
  column-gap: 5rem;
  row-gap: 1rem;
  padding-top: 2rem;
  padding-bottom: 2rem;
}

.projects {
  margin: 1em 0 2em;
}
</style>
