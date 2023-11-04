<script setup lang="ts">
  import { cn } from '@/utils/index'
</script>

<template>
  <span
    :class="
      cn(
        'ml-auto text-xs tracking-widest text-neutral-500 dark:text-neutral-400',
        $attrs.class ?? '',
      )
    "
  >
    <slot />
  </span>
</template>
