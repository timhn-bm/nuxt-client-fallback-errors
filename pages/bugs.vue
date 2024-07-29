<script setup lang="ts">
import ErrorBoundary from "~/components/ErrorBoundary.vue";
import A from "../components/A.vue";

import B from "../components/B.vue";

import C from "../components/C.vue";
</script>

<template>
  <div style="display: flex; flex-direction: column; gap: 16px">
    <ErrorBoundary>
      <A />

      <template #error> an error occurred in A </template>
    </ErrorBoundary>

    <ErrorBoundary>
      <B />

      <template #error> an error occurred in B </template>
    </ErrorBoundary>

    <ErrorBoundary>
      <C />

      <template #error>
        <div>an error occurred in C</div>
      </template>
    </ErrorBoundary>
  </div>
</template>
