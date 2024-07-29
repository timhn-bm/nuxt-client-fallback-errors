<script setup lang="ts">
import A from "../components/A.vue";

import B from "../components/B.vue";

import C from "../components/C.vue";
</script>

<template>
  <div style="display: flex; flex-direction: column; gap: 16px">
    <NuxtClientFallback :keep-fallback="true">
      <A />

      <template #fallback> an error occurred in A </template>
    </NuxtClientFallback>

    <NuxtClientFallback :keep-fallback="true">
      <B />

      <template #fallback> an error occurred in B </template>
    </NuxtClientFallback>

    <NuxtClientFallback :keep-fallback="true">
      <C />

      <template #fallback>
        <div>an error occurred in C</div>
      </template>
    </NuxtClientFallback>
  </div>
</template>
