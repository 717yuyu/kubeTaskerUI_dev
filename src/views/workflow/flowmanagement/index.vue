<template>
  <div class="p-4">
    <GrowCard :loading="loading" class="enter-y" />
    <SiteAnalysis class="!my-4 enter-y" :loading="loading" />
  </div>
</template>
<script lang="ts" setup>
  import { ref } from 'vue';
  import GrowCard from './components/GrowCard.vue';
  import SiteAnalysis from './components/SiteAnalysis.vue';
  import {applyReactInVue, applyPureReactInVue} from 'veaury';

  const loading = ref(true);

  setTimeout(() => {
    loading.value = false;
  }, 1500);
</script>
