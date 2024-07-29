<script lang="ts" setup></script>

<template>
  <NuxtClientFallback :keep-fallback="true">
    <slot> </slot>

    <template #fallback>
      <div style="background: red; color: white; padding: 10px">
        <slot name="error"> </slot>
      </div>
    </template>
  </NuxtClientFallback>
</template>
