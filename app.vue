<script setup lang="ts">
import { SpeedInsights } from '@vercel/speed-insights/nuxt'
import { initFlowbite } from 'flowbite'
import { APP_URL } from './settings/constants';

const { $pwa } = useNuxtApp()

const $route = useRoute()

useHead(() => {
  link: [
    {
      rel: 'canonical',
      href: APP_URL + $route.path
    }
  ]
})

onMounted(async () => {
  if (!$pwa) {
    return
  }

  if ($pwa.offlineReady) {
    alert('App is ready to work offline')
  }

  if ($pwa.isInstalled) {
    // alert('App is installed')

    if ($pwa.needRefresh) {
      alert('App has update available')

      await $pwa.updateServiceWorker()
      await $pwa.install()
    }
  } else {
    $pwa.showInstallPrompt = true
    $pwa.install()
  }

  // $pwa.update()
})

onBeforeMount(() => {
  initFlowbite()
})
</script>

<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
