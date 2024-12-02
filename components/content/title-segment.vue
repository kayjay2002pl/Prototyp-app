<script lang="ts">
export default {
  name: 'title-segment'
}
</script>

<template>
  <div class="relative w-full pt-[55%]">

    <button @click="navigateTo('/')" class="z-10 absolute top-0 bg-white w-full pt-[45%] mt-10 skew-y-3">
      <nuxt-img style="margin: 0px;" class="-skew-y-3 absolute top-[55%] left-1/2 transform -translate-x-1/2 -translate-y-1/2 px-4" src="img/strona2transparent.png" alt="absc" />
    </button>
    <div class="z-50 relative flex flex-col md:flex-row w-full mt-4">
      <button class="flex flex-1 justify-center font-bold text-2xl" @click="navigateTo('/wydarzenia')">wydarzenia</button>
      <button class="flex flex-1 justify-center font-bold text-2xl" @click="navigateTo('/about')">o nas</button>
      <button class="flex flex-1 justify-center font-bold text-2xl" @click="navigateTo('/kontakt')">kontakt</button>
    </div>
  </div>
</template>
