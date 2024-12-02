<script setup lang="ts">
import EmptyDoc from '~/components/slots/empty-doc.vue'
import NotFound from '~/components/slots/not-found.vue'

const $runtime = useRuntimeConfig()

useHead({
  title: $runtime.public.APP_TITLE
})
</script>

<template>
  <div class="index-page content-page markdown-content flex flex-col w-full flex-1">
    <main class="w-full px-0 overflow-y-auto">
      <div class=" w-full">
        <TitleSegment/>
        <h2>
          Archiwum Wydarzeń
        </h2>
        <EventPreview v-for="x in 6" :eventid="x"/>
      </div>
      
    </main>
  </div>
</template>
