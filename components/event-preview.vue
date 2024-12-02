<script setup lang="ts">
const $props = defineProps({
  eventid: {
    required: true
  }
})
const data = [
  {
    title: 'JAK ZROBIĆ GAZETĘ? - PROTOTYP happening + premiera 3 numeru kwartalnika prototyp',
    link:'https://www.facebook.com/events/343935928590870/'
  },
  {
    title: 'PROTOTYP PREMIERY CZTERY - premiera czwartego numeru kwartalnika prototyp + wystawa i licytacja prac z wydarzenia JAK ZROBIĆ GAZETĘ? – PROTOTYP 3,5',
    link:'https://www.facebook.com/events/436353002209157/'
  },
  {
    title: 'Finisaż Pystawy Prototypu',
    link:'https://www.facebook.com/events/1182608542875369/'
  },
  {
    title: 'PROTOTYP 1/4 TREŚĆ - premiera szóstego prototypu + zbieranie treści do następnego numeru',
    link:'https://www.facebook.com/events/1222358742426209/'
  },
  {
    title: 'PROTOTYP 2/4 FORMA',
    link:'https://www.facebook.com/events/531920536219894/'
  },
  {
    title: 'PROTOTYP 3/4 PROCES',
    link:'https://www.facebook.com/events/925099399505707/'
  },
]
</script>

<template>
  <button class="relative w-full px-8 mb-8">
    <NuxtImg @click="navigateTo(data[$props.eventid as number].link, {external: true})" :src="`img/wydarzenie${$props.eventid}.jpg`"></NuxtImg>
    <h3>{{ data[($props.eventid as number) -1].title }}</h3>
    
    
  </button>
</template>
