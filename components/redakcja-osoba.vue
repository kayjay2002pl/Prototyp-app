<script setup lang="ts">
const $props = defineProps({
  eventid: {
    required: true
  }
})
const data = [
  {
    imie: 'Konrad Pokrywka',
    opis:'sklejam makiety szybciej niż skręcam papierosy'
  },
  {
    imie: 'Mila Antoniszczak',
    opis:'Robię magistra ze studiowania na pierwszym roku'
  },
  {
    imie: 'Hubert Grzyb',
    opis:'szukam pracy \n ig: betonposting \n ps. konrad wolno kręci'
  },
  {
    imie: 'Zuzia Pruchniak',
    opis:'Twoje szczęśliwe numery na dziś to 4 i 20'
  },
]
</script>

<template>
  <button class="flex flex-col items-center w-full px-8 mb-8">
    <img src="public/img/fishplaceholder.gif"></img>
    <h3>{{ data[($props.eventid as number) -1].imie }}</h3>
    <h4>{{ data[($props.eventid as number) -1].opis }}</h4>
    
    
  </button>
</template>
