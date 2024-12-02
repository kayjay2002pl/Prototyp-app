<script setup lang="ts">
import EmptyDoc from '~/components/slots/empty-doc.vue'
import NotFound from '~/components/slots/not-found.vue'
import RedakcjaOsoba from '../components/redakcja-osoba.vue';

const $runtime = useRuntimeConfig()

useHead({
  title: $runtime.public.APP_TITLE
})
</script>

<template>
  <div class="index-page content-page markdown-content flex flex-col w-full flex-1">
    <main class="w-[100%] overflow-y-hidden px-0">
      <div class="w-full">
        <TitleSegment/>
        <h2>
          Redakcja
        </h2>
        <div class="grid grid-cols-1 md:grid-cols-2 gap4">
          <RedakcjaOsoba v-for="x in 4" :eventid="x"/>
        </div>
      
      </div>
      
    </main>
  </div>
</template>
