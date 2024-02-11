<script setup lang="ts">
import Greeting from '../components/home/Greeting.vue'
import WhoIAm from '../components/home/WhoIAm.vue'
import WhatIDo from '../components/home/WhatIDo.vue'
import WhatImInterestedIn from '../components/home/WhatImInterestedIn.vue'
import ContactMe from '../components/home/ContactMe.vue'
import YamlContent from 'data/config.yml'

const showWhoIAm = YamlContent.meta.facts[0].web
const showWhatIDo = YamlContent.meta.facts[1].web
const showWhatImInterestedIn = YamlContent.meta.facts[2].web
</script>

<template>
  <main>
    <Greeting />
    <span v-if="showWhoIAm"><WhoIAm /></span>
    <span v-if="showWhatIDo"><WhatIDo /></span>
    <span v-if="showWhatImInterestedIn"><WhatImInterestedIn /></span>
  </main>
  <ContactMe />
</template>
